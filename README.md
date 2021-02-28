# Event Sourcing

Events sourcing is the process of processing events that reflect changes maid to
a system after the fact. The concept is fairly simple but it's implementation
can be quite complex.

A very goo description - https://dev.to/barryosull/event-sourcing-what-it-is-and-why-its-awesome

Events sourcing has many benefits of being implemented using [CQRS]

Events can be called state transitions but preferable they are called events.
Never have getters and setters.


# How to use correlationID and causationID

__"From Greg Young"__

> Let's say every message has 3 ids. 1 is its id. Another is correlation, the
> last is causation. If you are responding to a message, you copy its
> correlation id as your correlation id, its message id is your causation id.
> This allows you to see an entire conversation (correlation id) or to see what
> causes what (causation id).

# Workflows, Sagas and Choreography

- [GOTO 2019 • Not Just Events: Developing Asynchronous Microservices • Chris Richardson](https://youtu.be/kyNL7yCvQQc?t=1277)

## Versioning

- [Versioning in an Event Sourced System book by Greg Young](https://leanpub.com/esversioning)

# Videos

- [Functional Programming with DDD](https://skillsmatter.com/skillscasts/3191-ddd-functional-programming)
- [[West LA Go Meetup] Jamie Isaacs - Event Modeling: From Sticky Notes to Go](https://www.youtube.com/watch?v=i7_edqzneyM)
- [GregYoung 8 CQRS Class](https://www.youtube.com/watch?v=whCk1Q87_ZI)

__CQRS and Event Sourcing Introduction with Greg Young__

- [Part - 1]: https://www.youtube.com/watch?v=AspkNFjhHIM
- [Part - 2]: https://www.youtube.com/watch?v=bkVV1eUMIs4
- [Part - 3]: https://www.youtube.com/watch?v=b9KNUCH6rH0
- [part - 4]: https://www.youtube.com/watch?v=o51kMltuSuQ


https://dev.to/barryosull/event-sourcing-what-it-is-and-why-its-awesome

[CQRS]: #CQRS

