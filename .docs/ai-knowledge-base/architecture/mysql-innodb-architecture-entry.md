# MySQL InnoDB Architecture — Knowledge Base Entry

## Role

This entry points to the authoritative InnoDB internals chapter in the database masterclass. It does not duplicate the technical analysis.

## Authoritative Document

- [MySQL InnoDB Architecture](../../../database/database-masterclass/02-relational-engines/02-mysql-innodb-architecture.md)

## Related Documents

- [PostgreSQL vs MySQL Comparison](../../../database/database-masterclass/02-relational-engines/03-postgres-vs-mysql-comparison.md)
- [Index Internals and Memory Layouts](../../../database/database-masterclass/02-relational-engines/04-index-internals-and-memory-layouts.md)
- [PostgreSQL vs MySQL Comparison Entry](./postgres-vs-mysql-comparison-entry.md)

## Decision Summary (Non-Substitutive)

InnoDB keeps current rows in the clustered index and reconstructs older snapshots via undo chains. Write-path pain typically appears as gap/next-key lock contention under range-heavy repeatable-read workloads, purge pressure when long transactions keep undo history alive, and flush or checkpoint pressure when dirty-page debt catches up. Buffer pool fit dominates predictable OLTP read latency. Replication mode and Vitess sharding are correctness and topology decisions, not only throughput knobs.

## Maintenance Note

When the masterclass InnoDB chapter evolves, update this entry only for link accuracy and the short decision summary. Keep mechanism-level explanation in the masterclass file.
