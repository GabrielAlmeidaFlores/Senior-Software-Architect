# PostgreSQL Deep Dive — Knowledge Base Entry

## Role

This entry points to the authoritative PostgreSQL internals chapter in the database masterclass. It does not duplicate the technical analysis.

## Authoritative Document

- [PostgreSQL Deep Dive](../../../database/database-masterclass/02-relational-engines/01-postgresql-deep-dive.md)

## Related Documents

- [PostgreSQL vs MySQL Comparison](../../../database/database-masterclass/02-relational-engines/03-postgres-vs-mysql-comparison.md)
- [Index Internals and Memory Layouts](../../../database/database-masterclass/02-relational-engines/04-index-internals-and-memory-layouts.md)
- [PostgreSQL vs MySQL Comparison Entry](./postgres-vs-mysql-comparison-entry.md)

## Decision Summary (Non-Substitutive)

PostgreSQL implements MVCC with heap tuple versions cleaned by vacuum. Under sustained mutation, vacuum lag produces table and index bloat, statistics drift, and plan regression. HOT updates reduce index churn when indexed columns are unchanged but do not remove vacuum need. Finite transaction IDs make freeze and anti-wraparound vacuum an availability concern. WAL-first durability and checkpoint policy trade commit/recovery behavior against write amplification.

## Maintenance Note

When the masterclass PostgreSQL chapter evolves, update this entry only for link accuracy and the short decision summary. Keep mechanism-level explanation in the masterclass file.
