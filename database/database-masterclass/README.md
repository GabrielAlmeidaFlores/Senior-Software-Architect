# Database Masterclass Index

## Scope

This masterclass is a multi-document reference for senior-level database architecture, distributed consistency trade-offs, storage-engine internals, and production selection frameworks.

This module is the **current phase** of the broader repository journey, which will later expand into Linux, cloud, and other core software engineering domains.

## Document Map

### 01 Theory and Foundations

- [CAP and PACELC Theorems](./01-theory-and-foundations/01-cap-pacelc-theorems.md)
- [ACID vs BASE Models](./01-theory-and-foundations/02-acid-vs-base-models.md)
- [Consensus, 2PC, and Distributed Transactions](./01-theory-and-foundations/03-consensus-2pc-and-distributed-transactions.md)
- [Quorum, Raft, and Paxos Internals](./01-theory-and-foundations/04-quorum-raft-paxos-internals.md)

### 02 Relational Engines

- [PostgreSQL Deep Dive](./02-relational-engines/01-postgresql-deep-dive.md)
- [MySQL InnoDB Architecture](./02-relational-engines/02-mysql-innodb-architecture.md)
- [PostgreSQL vs MySQL Comparison](./02-relational-engines/03-postgres-vs-mysql-comparison.md)
- [Index Internals and Memory Layouts](./02-relational-engines/04-index-internals-and-memory-layouts.md)

### 03 NoSQL Paradigms

- [NoSQL Taxonomy](./03-nosql-paradigms/01-nosql-taxonomy.md)
- [MongoDB Architecture](./03-nosql-paradigms/02-mongodb-architecture.md)
- [Columnar Databases and OLAP Architecture](./03-nosql-paradigms/03-columnar-databases-and-olap-architecture.md)
- [Key-Value Architecture and Design Decisions](./03-nosql-paradigms/04-key-value-architecture-and-design-decisions.md)
- [Graph Databases and Traversal Workloads](./03-nosql-paradigms/05-graph-databases-and-traversal-workloads.md)
- [Cassandra, CockroachDB, Redis, and PACELC Mapping](./03-nosql-paradigms/06-cassandra-cockroachdb-redis-and-pacelc-mapping.md)

### 04 Architectural Decision Framework

- [Database Selection Playbook](./04-architectural-decision-framework/01-database-selection-playbook.md)
- [Operational Excellence for Databases](./04-architectural-decision-framework/02-operational-excellence-for-databases.md)

## Visual Rule Compliance

Each domain document includes at least one Mermaid diagram to reinforce conceptual understanding with a visual representation of mechanisms, flows, or decision structures.

## External Visual References

For internet-based visual support and deeper exploration, documents include links to authoritative external resources and visual explainers where appropriate.

## Position in the Repository Roadmap

- Current phase: **Database and Distributed Data Systems**
- Next planned phases: **Linux Fundamentals**, **Cloud Architecture**, **Platform Reliability**

The intent is to build senior-level depth incrementally, one domain at a time, while preserving cross-links between topics.
