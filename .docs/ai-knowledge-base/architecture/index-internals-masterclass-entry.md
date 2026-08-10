# Index Internals and Memory Layouts — Knowledge Base Entry

## Role

This entry points to the authoritative index and storage-layout chapter in the database masterclass. It does not duplicate the technical analysis.

## Authoritative Document

- [Index Internals and Memory Layouts](../../../database/database-masterclass/02-relational-engines/04-index-internals-and-memory-layouts.md)

## Related Documents

- [PostgreSQL Deep Dive](../../../database/database-masterclass/02-relational-engines/01-postgresql-deep-dive.md)
- [MySQL InnoDB Architecture](../../../database/database-masterclass/02-relational-engines/02-mysql-innodb-architecture.md)
- [NoSQL Taxonomy](../../../database/database-masterclass/03-nosql-paradigms/01-nosql-taxonomy.md)

## Decision Summary (Non-Substitutive)

Index choice is a write-amplification, cache-residency, and tail-latency decision. B-trees favor balanced point/range reads with page-split maintenance under random inserts. LSM-trees favor ingest via WAL, memtable, SSTable flush, and compaction, at the cost of read amplification and compaction debt that can become compaction storms. Secondary indexes are permanent write taxes; composite key order must match usable leftmost prefixes. Operational failure modes include bloat/fragmentation, stale statistics, over-indexing, and tombstone pressure.

## Maintenance Note

When the masterclass index chapter evolves, update this entry only for link accuracy and the short decision summary. Keep mechanism-level explanation in the masterclass file.
