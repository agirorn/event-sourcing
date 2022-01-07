# notes

# Read up to an offset.

On update return an offset and read until the version has reached the offset.
This will remove the eventually consisted issues.

### How to use correlationID and causationID

__"From Greg Young"__

> Let's say every message has 3 ids. 1 is its id. Another is correlation, the
> last is causation. If you are responding to a message, you copy its
> correlation id as your correlation id, its message id is your causation id.
> This allows you to see an entire conversation (correlation id) or to see what
> causes what (causation id).

## Netflix has 135.000.000 users
Is your app at there scale and if not can you get a way with leaner architecture

## Links

- https://ookami86.github.io/event-sourcing-in-practice/#title.md
- https://kolodziejj.info/talks/es/
- https://leanpub.com/eventsourcinginpython
- https://github.com/johnbywater/eventsourcing
- https://eventsourcing.readthedocs.io/en/stable/topics/quick_start.html#define-model
- https://eventsauce.io/docs/event-sourcing/create-an-aggregate-root/
- https://kolodziejj.info/talks/es/
- https://leanpub.com/eventsourcinginpython
https://particular.net/blog/there-is-one-administrator?utm_source=announcement&utm_medium=email
https://microservices.io/book
https://developer.lightbend.com/docs/akka-platform-guide/microservices-tutorial/entity.html?utm_campaign=Oktopost-BLG+-+Akka+Platform+Guide&utm_content=Oktopost-twitter&utm_medium=social&utm_source=twitter
https://logcorner.com/building-microservices-through-event-driven-architecture-part13-read-model-projection-project-streams-into-elasticsearch/
https://www.eventstore.com/webinars/q-a-eventstoredb-event-sourcing-cqrs-and-ddd-jul-2020?utm_campaign=Q%26A%20-%20Mat%20%26%20Alexey&utm_content=151086059&utm_medium=social&utm_source=twitter&hss_channel=tw-703358826
https://jen20.com/2015/02/08/event-sourcing-in-go.html
https://medium.com/wardleymaps/on-being-lost-2ef5f05eb1ec
https://microservices.io/book
https://eventuate.io/exampleapps.html
https://eventuate.io/abouteventuatetram.html
https://github.com/eventuate-tram/eventuate-tram-examples-java-spring-todo-list/tree/master/single-module/src/main/java/io/eventuate/tram/examples/todolist
https://martinfowler.com/bliki/CQRS.html
https://martinfowler.com/bliki/EagerReadDerivation.html
https://docs.microsoft.com/en-us/azure/event-hubs/event-hubs-about
https://docs.microsoft.com/en-us/azure/event-hubs/event-hubs-node-get-started-send
https://www.quora.com/Is-CQRS-really-good?top_ans=73132309
https://danielwhittaker.me/2020/02/20/cqrs-step-step-guide-flow-typical-application/
https://thesaurus.yourdictionary.com/fact
https://zimarev.com/page/book/
https://zimarev.com/blog/event-sourcing/myth-busting/2020-07-09-overselling-event-sourcing/
https://lostechies.com/jimmybogard/2012/08/22/busting-some-cqrs-myths/
https://www.infoq.com/news/2020/02/event-sourcing-doomen-ddd-europe/
https://samnewman.io/talks/principles-of-microservices/
https://www.eventstore.com/
https://stackoverflow.com/questions/30721942/sql-join-across-multiple-tables-and-order-by-single-column
https://workers.cloudflare.com/
https://www.infoq.com/news/2020/10/svelte-edge-cloudflare-worker/
https://github.com/lukeed/uvu
https://www.youtube.com/watch?v=osk0ZBdBbx4
https://dev.to/barryosull/event-sourcing-what-it-is-and-why-its-awesome


## Event sourcing

According to [Software Architecture and Design InfoQ Trends Report—April 2020]
Event Sourcing is a being used by the Early Majority


## Links

- https://www.infoq.com/articles/architecture-trends-2020/
- https://www.infoq.com/eventsourcing/
- https://www.infoq.com/eventdrivenarchitecture/

## Event driver microservice

- Self-contained with clear interfaces and a distinct purpose
- Loosely coupled - communicate over a network
- Independently deployable, scalable, maintainable and testable

## Videos

- [Designing Events-First Microservices](https://www.youtube.com/watch?v=1hwuWmMNT4c)
- [Creating event-driven microservices: the why, how and what by Andrew Schofield](https://www.youtube.com/watch?v=ksRCq0BJef8)

### #GoogleCloudNext

- [Event-driven microservices with Cloud Run](https://www.youtube.com/watch?v=0N82S5fXpQE&feature=emb_logo




### Tools

#### Cloudevents

- https://cloudevents.io/

#### Knative

- https://knative.dev/
- https://cloud.google.com/knative
- [VIDEO](https://www.youtube.com/watch?v=riq0x5xdfNg)



## Eventual consistency

- https://www.allthingsdistributed.com/2008/12/eventually_consistent.html


[Software Architecture and Design InfoQ Trends Report—April 2020]: https://www.infoq.com/articles/architecture-trends-2020/
