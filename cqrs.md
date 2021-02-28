# CQRS

CQRS stands for Command Query Responsibility Segregation. When using CQRS you
use separate databases to store changes to a system that to query the system.

They main benefit of this kind of system is the grate separation between
changes maid in the system and reading and reporting on the changes maid in the
system.

Often this is used to populate read stores like elastic search or memcached.
