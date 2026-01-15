# Distributed Data Systems

This repository documents my work designing, reasoning about, and operating **distributed data systems** at scale.

The focus is on **architectural decision-making**, **trade-offs**, and **failure modes** across batch and streaming data platforms, ML/AI infrastructure, and foundational data platform components. The artifacts here reflect how similar problems recur across domains such as ads, financial data, and AI systems under different constraints.

This is not a tutorial repository. Code is included where it clarifies system behavior, but the primary emphasis is on **system design, correctness, scalability, and long-term operability**.

---

## Scope

The systems covered in this repository include:

- **Batch and streaming data processing**
  - Spark execution and failure semantics
  - Structured streaming design
  - Backfills, reprocessing, and late data handling

- **ML / AI infrastructure**
  - Feature store architectures
  - Offline vs online consistency
  - Training and inference pipelines
  - Model lineage and metadata

- **Platform infrastructure**
  - Lakehouse and storage engine design
  - Metadata and catalog systems
  - Multi-tenant isolation and performance
  - Cost and scalability trade-offs

- **Governance, privacy, and compliance**
  - Lineage at scale
  - Schema evolution and contracts
  - Auditability and access control

- **Operational learnings**
  - Postmortems
  - Scaling failures
  - Cost regressions
  - Design decisions that did *not* work

---

## Design principles

The work in this repository is guided by a few consistent principles:

- **Systems over pipelines**  
  Preference for platform thinking, clear ownership boundaries, and long-term maintainability.

- **Correctness before cleverness**  
  Especially in financial, ML, and regulatory contexts.

- **Explicit trade-offs**  
  Every design makes constraints visible: latency, cost, complexity, and failure domains.

- **Reality over abstraction**  
  Designs account for operational concerns: on-call load, backfills, schema drift, and human error.

---

## Repository structure

distributed-data-systems/
├── foundations/
│ ├── consistency-models.md
│ ├── exactly-once-semantics.md
│ └── schema-evolution.md
├── batch-and-streaming/
│ ├── spark-internals.md
│ ├── structured-streaming-design.md
│ └── backfills-at-scale.md
├── ml-infrastructure/
│ ├── feature-store-architecture.md
│ ├── offline-online-consistency.md
│ └── model-lineage.md
├── platform-infrastructure/
│ ├── lakehouse-storage-design.md
│ ├── metadata-systems.md
│ └── multi-tenant-isolation.md
├── governance-and-compliance/
│ ├── lineage-at-scale.md
│ ├── privacy-by-design.md
│ └── auditability.md
└── postmortems/
├── schema-change-outage.md
├── streaming-backpressure.md
└── cost-explosion.md


The structure reflects **problem classes**, not companies or tools. Individual artifacts may reference specific technologies (Spark, Kafka, Iceberg, cloud platforms) where necessary.

---

## Intended audience

This repository is written for:

- Staff+ data engineers and platform engineers
- Engineers designing or operating large-scale data systems
- Hiring committees evaluating architectural and systems thinking

It assumes familiarity with distributed systems concepts and modern data infrastructure.

---

## Relationship to market analysis

This work is informed by an analysis of global Staff+ data engineering roles across companies operating at significant scale. That analysis shaped the scope and weighting of topics here, but is intentionally kept separate from this repository.

(See linked repository for role and market research.)

---

## Status

This repository is actively evolving. Artifacts are added as systems are designed, stress-tested, or revisited with new constraints.

Feedback, discussion, and critical review are welcome.
