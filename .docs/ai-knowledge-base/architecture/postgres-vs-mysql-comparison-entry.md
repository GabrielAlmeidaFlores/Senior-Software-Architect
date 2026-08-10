# PostgreSQL vs MySQL Comparison — Knowledge Base Entry

## Role

This entry points to the authoritative comparison document in the database masterclass. It does not duplicate the technical analysis.

## Authoritative Document

- [PostgreSQL vs MySQL (InnoDB): Deep Architectural Comparison](../../../database/database-masterclass/02-relational-engines/03-postgres-vs-mysql-comparison.md)

## Related Engine Internals

- [PostgreSQL Deep Dive](../../../database/database-masterclass/02-relational-engines/01-postgresql-deep-dive.md)
- [MySQL InnoDB Architecture](../../../database/database-masterclass/02-relational-engines/02-mysql-innodb-architecture.md)
- [Sharding, Data Partitioning, and Horizontal Database Scale](../../../database/database-masterclass/01-theory-and-foundations/05-sharding-data-partitioning-and-horizontal-scale.md)

## Decision Summary (Non-Substitutive)

Engine choice is workload-constrained and team-constrained. Under write-heavy load, PostgreSQL’s first-order operational risk is vacuum lag leading to heap/index bloat and plan drift; InnoDB’s first-order risks are gap/next-key lock contention under range-heavy repeatable-read writes and purge pressure from long-lived undo history. Read-heavy advantages diverge by query complexity versus predictable buffer-pool OLTP paths, and both engines require explicit replica lag policy for read scaling.

## Maintenance Note

When the masterclass comparison document evolves, update this entry only for link accuracy and the short decision summary. Keep mechanism-level explanation in the masterclass file.
