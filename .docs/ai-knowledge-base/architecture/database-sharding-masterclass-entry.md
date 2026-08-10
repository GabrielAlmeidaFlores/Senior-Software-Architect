# Database Sharding Masterclass Entry

## Purpose and Context

This entry makes the database sharding chapter discoverable from the AI-maintained knowledge base while keeping the masterclass chapter as the single authoritative explanation. It records that the repository treats sharding as a data-ownership and operational-reliability decision, not as an automatic response to traffic growth.

## Authoritative Document

Read [Sharding, Data Partitioning, and Horizontal Database Scale](../../../database/database-masterclass/01-theory-and-foundations/05-sharding-data-partitioning-and-horizontal-scale.md) for the mechanism-level discussion of partition keys, routing, migration, hotspots, cross-shard work, and recovery.

The chapter was motivated by [Database Sharding / Fragmentation](https://www.youtube.com/watch?v=xJllDyCIyws). The source is useful as an introduction, but the repository corrects its unsafe simplifications: deterministic hashes need not be reversible, Sagas are semantic compensation rather than rollback, and service decomposition is independent from database sharding.

## Knowledge Graph

The sharding chapter depends on [CAP and PACELC](../../../database/database-masterclass/01-theory-and-foundations/01-cap-pacelc-theorems.md) for availability and latency trade-offs, [Consensus, 2PC, and Distributed Transactions](../../../database/database-masterclass/01-theory-and-foundations/03-consensus-2pc-and-distributed-transactions.md) for coordination failure semantics, and [MongoDB Architecture](../../../database/database-masterclass/03-nosql-paradigms/02-mongodb-architecture.md) for a concrete native-sharding topology.

The boundary is intentional. This entry is a navigational record and decision context, while the linked masterclass chapter owns the technical content. Keeping that separation prevents divergent explanations as the knowledge base evolves.
