# 📘 Fundamentals of Data Engineering — Complete Study Roadmap

**Book:** *Fundamentals of Data Engineering* by Joe Reis & Matt Housley  
**Duration:** 65 days (~2.2 months)  
**Pace:** 1 session per day, ~45–75 min each  
**Start Date:** __________ (fill in your Day 1)

---

## 🗺️ Book Structure Overview

| Part | Chapters | Focus | Days |
|------|----------|-------|------|
| **Part I** — Foundation & Building Blocks | Ch 1–4 | What DE is, the lifecycle, architecture, choosing tech | Days 1–18 |
| **Part II** — Lifecycle In Depth | Ch 5–9 | Source systems, storage, ingestion, transformation, serving | Days 19–52 |
| **Part III** — Security, Privacy & Future | Ch 10–11 | Security best practices, future trends | Days 53–58 |
| **Appendices** | A & B | Serialization/compression, cloud networking | Days 59–61 |
| **Capstone & Review** | — | Final project, revision, mock interviews | Days 62–65 |

---

## 🏁 Milestones

| Milestone | Target Day | Checkpoint |
|-----------|-----------|------------|
| **M1** — Foundations Complete | Day 18 | Can explain the DE lifecycle, undercurrents, and architecture principles |
| **M2** — Source Systems + Storage Mastered | Day 30 | Understand databases, files, APIs, storage systems, and trade-offs |
| **M3** — Ingestion + Transformation Done | Day 45 | Can describe batch vs streaming, ETL vs ELT, data modeling approaches |
| **M4** — Full Lifecycle Complete | Day 52 | Can design an end-to-end pipeline on paper |
| **M5** — Book Finished + Capstone | Day 65 | Can explain all concepts, have a portfolio project |

---

## 📅 Daily Study Plan

### ═══════════════════════════════════════
### PART I: FOUNDATION & BUILDING BLOCKS
### ═══════════════════════════════════════

---

### Chapter 1: Data Engineering Described (Days 1–5)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **1** | What is Data Engineering? + DE Defined + The Data Engineering Lifecycle (intro) | pp. 3–6 |
| **2** | Evolution of the Data Engineer (history: data warehousing → big data → modern DE) | pp. 6–11 |
| **3** | DE & Data Science relationship + DE Skills & Activities + Data Maturity Model | pp. 11–17 |
| **4** | Background & Skills of a DE + Business vs Technical Responsibilities + Type A vs Type B engineers | pp. 17–22 |
| **5** | DEs inside organizations + Working with other roles (analysts, ML engineers, DevOps, leadership) | pp. 22–32 |

> **🧪 Mini-Project Seed (Day 5):** Write a 1-page doc describing a fictional company's data maturity level and what a DE would do there.

---

### Chapter 2: The Data Engineering Lifecycle (Days 6–11)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **6** | The DE Lifecycle overview + Generation: Source Systems | pp. 33–38 |
| **7** | Storage + Ingestion stages (key considerations for each) | pp. 38–43 |
| **8** | Transformation + Serving Data (analytics, ML, reverse ETL) | pp. 43–48 |
| **9** | Undercurrents: Security + Data Management (metadata, data quality, governance, master data) | pp. 48–59 |
| **10** | Undercurrents: DataOps + Data Architecture + Orchestration + Software Engineering | pp. 59–68 |
| **11** | 🔄 **WEEK 1–2 REVIEW** — Summary of Ch 1 & 2, mini mock interview, applied exercise | — |

> **🧪 Mini-Project Seed (Day 11):** Draw the full DE lifecycle diagram from memory and label every stage and undercurrent.

---

### Chapter 3: Designing Good Data Architecture (Days 12–16)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **12** | What is Data Architecture? + Enterprise Architecture + Data Architecture Defined + "Good" Architecture | pp. 71–77 |
| **13** | Principles of Good Data Architecture (all 9 principles: common components, failure, scalability, leadership, always be architecting, loose coupling, reversible decisions, security, FinOps) | pp. 77–87 |
| **14** | Major Architecture Concepts: Domains & services, distributed systems, tight vs loose coupling, tiers, monoliths, microservices, event-driven architecture, brownfield vs greenfield | pp. 87–98 |
| **15** | Architecture Examples: Data Warehouse, Data Lake, Convergence/Data Lakehouse, Modern Data Stack, Lambda & Kappa Architecture, Dataflow Model | pp. 98–106 |
| **16** | Architecture Examples (cont.): IoT Architecture, Data Mesh + Who designs architecture? | pp. 106–111 |

> **🧪 Mini-Project Seed (Day 16):** Compare Data Warehouse vs Data Lake vs Data Lakehouse in a table with trade-offs.

---

### Chapter 4: Choosing Technologies (Days 17–18)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **17** | Team size, speed to market, interoperability, cost optimization (TCO, TOCO, FinOps) + Immutable vs transitory tech + Location decisions (on-prem, cloud, hybrid, multicloud, edge) | pp. 115–132 |
| **18** | Build vs Buy (OSS, proprietary) + Monolith vs Modular + Serverless vs Servers + Benchmarks + Undercurrents impact on tech choices | pp. 132–151 |

> **Milestone M1 reached! ✅** You now understand the DE landscape, lifecycle, architecture, and how to choose tools.

---

### ═══════════════════════════════════════
### PART II: THE DATA ENGINEERING LIFECYCLE IN DEPTH
### ═══════════════════════════════════════

---

### Chapter 5: Data Generation in Source Systems (Days 19–25)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **19** | Sources of data + Source system main ideas: Files, APIs, Application Databases (OLTP) | pp. 155–159 |
| **20** | OLAP systems + Change Data Capture + Logs + Database Logs + CRUD vs Insert-Only | pp. 159–163 |
| **21** | Messages and Streams + Types of Time (event time, processing time, ingestion time) | pp. 163–165 |
| **22** | Source System Practical Details: Databases deep-dive (RDBMS, NoSQL types, graph, time-series, etc.) | pp. 165–174 |
| **23** | APIs + Data Sharing + Third-Party Sources + Message Queues & Event-Streaming Platforms (Kafka, etc.) | pp. 174–181 |
| **24** | Working with stakeholders + Undercurrents impact on source systems | pp. 181–187 |
| **25** | 🔄 **WEEK 3–4 REVIEW** — Summary of Ch 3, 4, 5. Mock interview. Applied exercise. | — |

> **🧪 Mini-Project Seed (Day 25):** Design a source system diagram for an e-commerce app (users, orders, products, events).

---

### Chapter 6: Storage (Days 26–33)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **26** | Raw Ingredients: Magnetic disk, SSD, RAM + Networking & CPU for storage | pp. 189–195 |
| **27** | Serialization + Compression + Caching | pp. 195–197 |
| **28** | Data Storage Systems: Single vs Distributed, Consistency models + File Storage (HDFS history, local/network) | pp. 197–202 |
| **29** | Block Storage + Object Storage (S3, GCS, Azure Blob — how they work, consistency, versioning, tiers) | pp. 202–211 |
| **30** | Cache/Memory-based storage + HDFS + Streaming Storage + Indexes, Partitioning, Clustering | pp. 211–215 |

> **Milestone M2 reached! ✅**

| **31** | Storage Abstractions: Data Warehouse vs Data Lake vs Data Lakehouse vs Data Platform + Stream-to-Batch | pp. 215–218 |
| **32** | Big Ideas: Data Catalogs, Data Sharing, Schema, Separation of Compute & Storage, Data Retention, Multi-tenant | pp. 218–227 |
| **33** | Stakeholders + Undercurrents impact on storage | pp. 227–231 |

> **🧪 Mini-Project Seed (Day 33):** Design a storage architecture for your e-commerce project (choose object store + warehouse + justify decisions).

---

### Chapter 7: Ingestion (Days 34–40)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **34** | What is Data Ingestion? + Key Considerations: Bounded vs Unbounded, Frequency, Sync vs Async | pp. 233–239 |
| **35** | Throughput, Reliability, Durability, Payload (kind, shape, size) + Push vs Pull vs Poll | pp. 239–244 |
| **36** | Batch Ingestion: Snapshot vs Differential, File-based, ETL vs ELT, Inserts/Updates, Data Migration | pp. 244–248 |
| **37** | Streaming Ingestion: Schema evolution, late-arriving data, ordering, replay, TTL, dead-letter queues | pp. 248–250 |
| **38** | Ways to Ingest Data: Direct DB connection, CDC, APIs, Message Queues, Managed Connectors, Object Storage, EDI | pp. 250–258 |
| **39** | Practical: File formats, Shell, SSH, SFTP, Webhooks, Web Scraping, Transfer Appliances, Data Sharing + Undercurrents | pp. 258–269 |
| **40** | 🔄 **WEEK 5–6 REVIEW** — Summary of Ch 6 & 7. Mock interview. Applied exercise. | — |

> **🧪 Mini-Project Seed (Day 40):** Design an ingestion pipeline: batch (daily CSV export) + real-time (Kafka events) for your e-commerce project.

---

### Chapter 8: Queries, Modeling, and Transformation (Days 41–49)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **41** | Queries: What is a query? Life of a query, Query optimizer | pp. 271–275 |
| **42** | Improving Query Performance: Indexes, pruning, predicate pushdown, prejoining, caching, CTEs, temp tables, views | pp. 275–281 |
| **43** | Queries on Streaming Data: Windowed joins, watermarks, combining streams, streaming buffers | pp. 281–287 |
| **44** | Data Modeling: Conceptual, Logical, Physical models + Normalization (1NF, 2NF, 3NF) | pp. 287–294 |

> **Milestone M3 reached! ✅** (Day 45)

| **45** | Batch Analytical Modeling: Kimball (star schema, facts & dimensions), Inmon, Data Vault | pp. 294–305 |
| **46** | Wide tables + One Big Table + Modeling Streaming Data | pp. 305–309 |
| **47** | Batch Transformations: SQL-based (ETL, ELT, dbt), distributed joins, broadcast joins, shuffle hash joins | pp. 309–318 |
| **48** | More Batch Transforms: MapReduce legacy, data wrangling, deletion/updates, DAGs + Materialized Views, Federation, Query Virtualization | pp. 318–326 |
| **49** | Streaming Transformations & Processing: Micro-batch vs true streaming, Streaming DAGs + Undercurrents | pp. 326–335 |

> **🧪 Mini-Project Seed (Day 49):** Model your e-commerce data using a star schema (identify fact and dimension tables, write example SQL).

---

### Chapter 9: Serving Data (Days 50–52)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **50** | General Considerations: Trust, Use Cases, Data Products, Self-Service, Data Definitions, Data Mesh + Analytics (Business, Operational, Embedded) | pp. 337–349 |
| **51** | Machine Learning considerations + Ways to Serve Data (Files, Databases, Streaming, Federation, Sharing, Semantic Layers, Notebooks) | pp. 349–358 |
| **52** | Reverse ETL + Stakeholders + Undercurrents | pp. 358–365 |

> **Milestone M4 reached! ✅** You can now trace data from source to serving!

---

### ═══════════════════════════════════════
### PART III: SECURITY, PRIVACY & THE FUTURE
### ═══════════════════════════════════════

---

### Chapter 10: Security and Privacy (Days 53–55)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **53** | People: Negative thinking, paranoia + Processes: Security theater vs habit, active security, least privilege, shared responsibility, backups, example policy | pp. 369–374 |
| **54** | Technology: Patching, encryption, logging/monitoring/alerting, network access + Security for low-level DE | pp. 374–378 |
| **55** | 🔄 **WEEK 7–8 REVIEW** — Summary of Ch 8, 9, 10. Mock interview. Applied exercise. | — |

> **🧪 Mini-Project Seed (Day 55):** Add security layers to your e-commerce pipeline (encryption at rest/transit, IAM roles, least privilege).

---

### Chapter 11: The Future of Data Engineering (Days 56–58)

| Day | Topic | Section(s) |
|-----|-------|------------|
| **56** | Lifecycle isn't going away + Decline of complexity + Cloud-scale Data OS + Improved interoperability + "Enterprisey" DE | pp. 379–384 |
| **57** | Evolving titles + Live Data Stack + Streaming pipelines + Real-time analytical DBs + Fusion of data with apps | pp. 384–388 |
| **58** | Tight feedback (apps ↔ ML) + Dark matter data + Rise of spreadsheets + Conclusion | pp. 388–389 |

---

### ═══════════════════════════════════════
### APPENDICES
### ═══════════════════════════════════════

| Day | Topic | Section(s) |
|-----|-------|------------|
| **59** | Appendix A: Serialization Formats (CSV, XML, JSON/JSONL, Avro, Parquet, ORC, Arrow) + Table management (Hudi, Iceberg, Delta) | pp. 391–396 |
| **60** | Appendix A (cont.): Compression (gzip, bzip2, Snappy, Zstandard, LZ4) + Appendix B: Cloud Networking (topology, egress costs, performance tiers) | pp. 396–402 |

---

### ═══════════════════════════════════════
### CAPSTONE & FINAL REVIEW
### ═══════════════════════════════════════

| Day | Activity |
|-----|----------|
| **61** | 🏗️ **Capstone Project Day 1** — Finalize end-to-end pipeline design for your e-commerce project (architecture diagram + tech choices + justification) |
| **62** | 🏗️ **Capstone Project Day 2** — Write detailed specs: ingestion, transformation, storage, modeling, serving layers |
| **63** | 📝 **Full Book Revision** — Review all chapter summaries, key terms, and diagrams |
| **64** | 🎤 **Mock Interview Marathon** — 20 DE interview questions covering all chapters |
| **65** | 🎓 **Graduation Day** — Final self-assessment, identify weak areas, plan next steps |

---

## 🔄 Weekly Review Schedule

| Review | Day | Covers |
|--------|-----|--------|
| Week 1–2 Review | Day 11 | Chapters 1–2 |
| Week 3–4 Review | Day 25 | Chapters 3–5 |
| Week 5–6 Review | Day 40 | Chapters 6–7 |
| Week 7–8 Review | Day 55 | Chapters 8–10 |
| Final Review | Day 63 | Entire Book |

**Each review session includes:**
1. Summary of all concepts from that period
2. 5-question mini mock interview
3. 1 applied mini-project idea

---

## 🏗️ Progressive Project: E-Commerce Data Platform

Your long-running project builds across the entire book:

| Phase | When | What You Build |
|-------|------|----------------|
| **Phase 1: Design** | Days 5–11 | Identify data sources, draw lifecycle diagram |
| **Phase 2: Source Systems** | Days 19–25 | Design source system schemas (OLTP DB, event streams, APIs) |
| **Phase 3: Storage** | Days 26–33 | Choose storage layers (S3 + Snowflake/BigQuery), justify decisions |
| **Phase 4: Ingestion** | Days 34–40 | Design batch + streaming ingestion (Airbyte/Fivetran + Kafka) |
| **Phase 5: Transformation** | Days 41–49 | Build star schema model, write dbt-style transformations |
| **Phase 6: Serving** | Days 50–52 | Design analytics dashboards, ML feature store, reverse ETL |
| **Phase 7: Security** | Days 53–55 | Add IAM, encryption, monitoring |
| **Phase 8: Capstone** | Days 61–62 | Complete architecture doc with all layers |

---

## 🛠️ Tool Mapping (Book Concepts → Industry Tools)

| Concept | Real-World Tools |
|---------|-----------------|
| Source Systems / OLTP | PostgreSQL, MySQL, MongoDB |
| Ingestion (Batch) | Airbyte, Fivetran, AWS Glue, Stitch |
| Ingestion (Streaming) | Apache Kafka, Amazon Kinesis, Pulsar |
| Storage (Object) | Amazon S3, Google Cloud Storage, Azure Blob |
| Storage (Warehouse) | Snowflake, BigQuery, Redshift, Databricks |
| Storage (Lake/Lakehouse) | Delta Lake, Apache Iceberg, Apache Hudi |
| Transformation | dbt, Apache Spark, SQL in warehouse |
| Orchestration | Apache Airflow, Dagster, Prefect, Mage |
| Serving (BI) | Looker, Tableau, Power BI, Metabase |
| Serving (ML) | Feature stores (Feast), MLflow |
| Data Quality | Great Expectations, Soda, Monte Carlo |
| Data Catalog | DataHub, Amundsen, Atlan |
| Reverse ETL | Census, Hightouch |
| Security | AWS IAM, HashiCorp Vault |

---

## 📌 How to Use This Roadmap

1. **Each day**, say: *"Start today's lesson"* or *"Continue from where we left off"*
2. I will deliver the lesson following the daily session format
3. On review days, I'll provide summaries + mock interviews + project ideas
4. Track your current day by updating the table above
5. If you need to skip a day, we simply pick up where we left off

---

## ✅ Progress Tracker

| Day | Date | Topic | Status |
|-----|------|-------|--------|
| 1 | | What is Data Engineering? | ✅  |
| 2 | | Evolution of the Data Engineer | ⬜ |
| 3 | | DE & Data Science + Data Maturity | ⬜ |
| 4 | | DE Skills + Type A vs B | ⬜ |
| 5 | | DEs in Organizations | ⬜ |
| 6 | | DE Lifecycle + Source Systems | ⬜ |
| 7 | | Storage + Ingestion stages | ⬜ |
| 8 | | Transformation + Serving | ⬜ |
| 9 | | Undercurrents: Security + Data Mgmt | ⬜ |
| 10 | | Undercurrents: DataOps + Architecture + Orchestration | ⬜ |
| 11 | | 🔄 Week 1–2 Review | ⬜ |
| 12 | | Data Architecture Defined | ⬜ |
| 13 | | 9 Principles of Good Architecture | ⬜ |
| 14 | | Architecture Concepts | ⬜ |
| 15 | | Architecture Examples (Warehouse, Lake, etc.) | ⬜ |
| 16 | | IoT, Data Mesh, Conclusion | ⬜ |
| 17 | | Choosing Tech: Cost, Location, Cloud | ⬜ |
| 18 | | Build vs Buy, Serverless, Benchmarks | ⬜ |
| 19 | | Source Systems: Files, APIs, OLTP | ⬜ |
| 20 | | OLAP, CDC, Logs, CRUD | ⬜ |
| 21 | | Messages, Streams, Types of Time | ⬜ |
| 22 | | Database Deep-Dive | ⬜ |
| 23 | | APIs, Kafka, Event-Streaming | ⬜ |
| 24 | | Stakeholders + Undercurrents | ⬜ |
| 25 | | 🔄 Week 3–4 Review | ⬜ |
| 26 | | Storage: Disk, SSD, RAM | ⬜ |
| 27 | | Serialization, Compression, Caching | ⬜ |
| 28 | | Storage Systems: Distributed, Consistency, File Storage | ⬜ |
| 29 | | Block + Object Storage | ⬜ |
| 30 | | Memory Storage, HDFS, Indexes, Partitioning | ⬜ |
| 31 | | Storage Abstractions | ⬜ |
| 32 | | Big Ideas in Storage | ⬜ |
| 33 | | Storage Stakeholders + Undercurrents | ⬜ |
| 34 | | Ingestion: Bounded/Unbounded, Frequency, Sync/Async | ⬜ |
| 35 | | Throughput, Reliability, Payload, Push/Pull | ⬜ |
| 36 | | Batch Ingestion Patterns | ⬜ |
| 37 | | Streaming Ingestion Patterns | ⬜ |
| 38 | | Ways to Ingest: CDC, APIs, Queues, Connectors | ⬜ |
| 39 | | Practical Ingestion + Undercurrents | ⬜ |
| 40 | | 🔄 Week 5–6 Review | ⬜ |
| 41 | | Queries: Basics + Optimizer | ⬜ |
| 42 | | Query Performance | ⬜ |
| 43 | | Streaming Queries | ⬜ |
| 44 | | Data Modeling + Normalization | ⬜ |
| 45 | | Star Schema, Inmon, Data Vault | ⬜ |
| 46 | | Wide Tables + Streaming Models | ⬜ |
| 47 | | Batch Transformations (SQL, dbt, joins) | ⬜ |
| 48 | | More Transforms: MapReduce, DAGs, Materialized Views | ⬜ |
| 49 | | Streaming Transforms + Undercurrents | ⬜ |
| 50 | | Serving: Trust, Analytics Types | ⬜ |
| 51 | | ML Serving + Ways to Serve Data | ⬜ |
| 52 | | Reverse ETL + Undercurrents | ⬜ |
| 53 | | Security: People + Processes | ⬜ |
| 54 | | Security: Technology | ⬜ |
| 55 | | 🔄 Week 7–8 Review | ⬜ |
| 56 | | Future: Complexity Decline, Interoperability | ⬜ |
| 57 | | Future: Live Data Stack, Streaming | ⬜ |
| 58 | | Future: Apps + ML Fusion, Conclusion | ⬜ |
| 59 | | Appendix A: Serialization Formats | ⬜ |
| 60 | | Appendix A + B: Compression + Cloud Networking | ⬜ |
| 61 | | 🏗️ Capstone Day 1 | ⬜ |
| 62 | | 🏗️ Capstone Day 2 | ⬜ |
| 63 | | 📝 Full Book Revision | ⬜ |
| 64 | | 🎤 Mock Interview Marathon | ⬜ |
| 65 | | 🎓 Graduation | ⬜ |

---

*Generated by your DE Mentor. Say "Start today's lesson" to begin Day 1!*
