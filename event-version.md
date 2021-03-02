# Event version

Event version should be added to event streams that have events that need to
have the data format changed so that the version of  the data format can be
identified.

- There is no need to add this to steams until events in the stream change in
  a way that affects the projections or replay of these events start to change.
- When events format is changed then the events can in many cases be cased to
  the new version. The case ca be done either for all events in the stream
  during a migration or in-flight when the event is being consumed.  In many
  cases casting to a new version in-flight is preferred since it requires no
  migration and not down time.

