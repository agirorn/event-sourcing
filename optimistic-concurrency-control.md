# Optimistic concurrency control

Optimistic concurrency control (OCC) can be used to block changes from being
applied to an aggregate out of order. This can be done by adding
a field "occVersion" field to the streams that needs to be non null and uniqe
for each event tin the stream.

- The occVersion field have to be unique for each aggregate and aggregate_id
  preventing any inserts into the stream that conflict with that constraint.
- The application that is generating and saving the events is responsible for
  adding the correct occVersion for the events it is adding.
- occVersion should not be confused with eventVersion.

### Links
- https://en.wikipedia.org/wiki/Optimistic_concurrency_control
- https://developers.eventstore.com/clients/dotnet/5.0/appending/optimistic-concurrency-and-idempotence.html#idempotence
