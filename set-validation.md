# set validation

Set validation is the process of validating business rules across multiple
aggregates. It can be done by replaying all evens to get the current state and
then do the validation. That only works for the smallest of apps and do not
scale. A Better way is to build some external mechanism that is kept up to date
on the write side and can be consulted to during the set validation.


## Unique email on users examples

Create a table with a single email_address column that has a unique constraint.
When adding a new adding a user or updating a users email address first in
try to insert the new email address into the email address table.
If that fail en abandon then entire command. If it is successful insert the
events and complete the transaction

```sql
create table users_unique_email_address_constraint (
  email text PRIMARY KEY -- constraint
);
```

```sql
BEGIN;
-- Only wait for a table lock for 1 sec
-- https://www.postgresql.org/docs/current/runtime-config-client.html#GUC-LOCK-TIMEOUT
SET lock_timeout=1000;

-- Only wait for a statement to complete for 1 sec
-- Ther prevents deadlocks when two or more clients try to add the same email
-- address at the same time
-- https://www.postgresql.org/docs/current/runtime-config-client.html#GUC-STATEMENT-TIMEOUT
SET statement_tmeout=1000;

-- Abort transactions that take more than a minute
-- this will remove transaction that are not completed when a client dies while
-- trying to perfom the transaction and was unable to commit it
-- https://www.postgresql.org/docs/current/runtime-config-client.html#GUC-IDLE-IN-TRANSACTION-SESSION-TIMEOUT
SET idle_in_transaction_session_timeout=60000;


-- Try to insert the email address to the unique email constraint table
INSERT INTO users_unique_email_address_constraint (email)
    VALUES ('address@example.com');

-- now you have a unique email address and can safely insert any events needed
-- by the command
INSERT INTO events (event_columns)
    VALUES (event_data);

-- Transaction is over
COMMIT;
```

### Unique email address

## Links

- https://stackoverflow.com/questions/9495985/cqrs-event-sourcing-validate-username-uniqueness
- https://danielwhittaker.me/2017/10/09/handle-set-based-consistency-validation-cqrs/
- https://dev.to/kspeakman/comment/ke6
- https://axoniq.io/blog-overview/set-based-validation?utm_campaign=Blog%20promotion&utm_source=twitter&utm_medium=social&utm_content=set%20based%20validation#0
