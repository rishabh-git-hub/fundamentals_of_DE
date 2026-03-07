# 📘 Day 6: The Data Engineering Lifecycle (Ch. 2) — Generation: Source Systems

**Book:** *Fundamentals of Data Engineering* — Chapter 2 (pp. 33–38)  
**Date:** ___________

---

## 🔄 Recap of Day 5

Completed Chapter 1. Deep-dived downstream relationships (DS need path to production, analysts are quality allies, ML eng boundaries are blurry). Team structures: centralized vs cross-functional vs hybrid. Kicked off ShopStream project Phase 1.

---

## The Lifecycle Framework

- 5 stages: Generation → Ingestion → Storage → Transformation → Serving
- 6 undercurrents: Security, Data Management, DataOps, Architecture, Orchestration, Software Engineering
- Stages can repeat, overlap, weave together — it's NOT always a neat linear flow
- Storage underlies ALL stages (foundation, not just a step)
- Data engineering lifecycle is a SUBSET of the full data lifecycle

---

## Generation: Source Systems

### Definition
- **Source system** = the origin of data used in the DE lifecycle
- Examples: IoT devices, application databases, message queues, APIs, SaaS platforms
- **DE consumes but does NOT own/control** source systems
- Must understand: how source generates data, frequency, velocity, variety, quirks

### Two Classic Patterns

**1. Application Database (Traditional)**
- App servers write to a database (PostgreSQL, MySQL, etc.)
- Stores **state** (current status of things)
- Pattern from 1980s, still dominant
- Modern evolution: microservices → many small DB pairs instead of one monolith

**2. IoT Swarm (Modern)**
- Fleet of devices sends messages to central collection system
- Produces a **stream** of events (things that happened)
- Collected via message queues (Kafka, Kinesis, Pulsar)

### Communication is Critical
- Keep open line with source system owners
- App code changes can break pipelines
- Schema changes, new databases, format changes — all can break things
- Never treat source systems as "someone else's problem"

---

## Evaluating Source Systems — The Checklist

| Category | Key Questions |
|----------|--------------|
| **Nature** | What kind of source? App DB? IoT? API? |
| **Persistence** | Long-term storage or temporary? |
| **Volume/Velocity** | Events/sec? GB/hour? |
| **Quality** | Consistency? Error rate? Duplicates? Late data? |
| **Schema** | What is the schema? Need to join across tables/systems? |
| **Schema Changes** | How communicated? How detected? |
| **Access** | Pull frequency? Snapshots vs CDC? |
| **Impact** | Will reading affect source performance? |
| **Dependencies** | Upstream dependencies of the source? |
| **Quality Checks** | Already in place at the source? |

**Critical warning:** Never run analytical queries on production databases — causes resource contention, slows app for real users. Use read replicas, CDC, or exports.

---

## The Schema Problem

### What is a Schema?
- Defines the hierarchical organization of data (tables, columns, types, relationships)
- Think: the "blueprint" of your data

### Fixed Schema vs Schemaless

| Fixed Schema | Schemaless |
|---|---|
| Database enforces structure | Application defines structure |
| Explicit ALTER TABLE to change | Can change at any time |
| Predictable ✅ | Flexible ✅ |
| Rigid ⚠️ | Unpredictable ⚠️ |
| Example: PostgreSQL, MySQL | Example: MongoDB, JSON files, message queues |

**Key insight:** "Schemaless doesn't mean the absence of schema" — the application defines the schema, not the database.

### Schema Evolution — #1 Source of Pipeline Breakage
- Schemas change over time (Agile encourages frequent changes)
- Common changes: new column, renamed column, type change, new table
- DE's job: take raw source schema → transform into analytics value
- This becomes much harder as schema evolves

### Defense Strategy
1. **Communicate** — regular syncs with source teams
2. **Detect** — auto-detect schema changes in ingestion tools
3. **Register** — schema registries for streaming data (track versions + history)
4. **Contract** — formal data contracts between producers and consumers
5. **Test** — automated tests catching schema drift
6. **Alert** — notifications for unexpected changes

---

## ShopStream Project — Source System Evaluation

| Source | Type | Schema | Volume | Key Risk |
|--------|------|--------|--------|----------|
| PostgreSQL | App DB, fixed schema | Medium risk (Agile team) | ~10K orders/day | Schema changes without notice |
| Clickstream | Event stream, schemaless JSON | HIGH risk | ~500K events/day | New event types, duplicates |
| Stripe API | 3rd party API, structured JSON | LOW risk (versioned) | Matches orders | Rate limits |
| Google Analytics | 3rd party SaaS | LOW risk | Daily aggregated | None major |
| Zendesk | 3rd party SaaS API | LOW risk | ~200 tickets/day | None major |

---

## Key Takeaways

1. Source systems are the origin of all data — DEs consume but don't own them
2. Two classic patterns: Application databases (state) vs IoT/event streams (events)
3. Always evaluate sources before building pipelines — use the checklist
4. Never query production databases for analytics — use replicas or CDC
5. Schema is your #1 pain source — it WILL change, plan for it
6. Fixed schema (DB enforces) vs schemaless (app controls) — both have trade-offs
7. Schema evolution breaks pipelines — communication + detection + registries are your defense

---

## Comprehension Questions

1. What is a source system? Why doesn't a DE own it?
2. Difference between app database source and IoT swarm source?
3. Name 5 evaluation questions and why each matters.
4. Fixed schema vs schemaless — why doesn't schemaless mean "no schema"?
5. What is schema evolution? Name two defense strategies.

---

## Practical Exercise

Pick any app on your phone. Write down:
1. What source systems does it have?
2. Fixed schema or schemaless for each?
3. One schema evolution risk
4. Three questions you'd ask the SW eng team before building a pipeline

---

## Tool Mapping

| Concept | Real Tool |
|---------|-----------|
| App database source | PostgreSQL, MySQL, MongoDB |
| IoT / event stream | Kafka, Kinesis, Pub/Sub |
| Third-party API | Stripe, Salesforce, GA APIs |
| Schema registry | Confluent Schema Registry, AWS Glue |
| Data contracts | Soda, DataContract CLI |
| Managed connectors | Fivetran, Airbyte (auto schema detection) |
| Safe querying | AWS RDS Read Replicas, Cloud SQL Replicas |

---

*Next: Day 7 — Storage + Ingestion Stages (Chapter 2 continued)*
