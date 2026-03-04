# 📘 Day 3: Data Engineering & Data Science + DE Skills & Activities + Data Maturity Model

**Book:** *Fundamentals of Data Engineering* — Chapter 1 (pp. 11–17)  
**Date:** ___________

---

## 🔄 Recap of Day 2

Four eras of data engineering: Data Warehousing (1980s–2000) → Birth of Contemporary DE (Google papers, Hadoop, AWS) → Big Data Era (Hadoop ecosystem, hype, data swamps) → Modern Era (cloud-first, managed services, simplification). Modern DEs focus on the lifecycle, not managing clusters.

---

## Part 1: Data Engineering vs Data Science

### Key Relationship
- **Data Engineering is SEPARATE from Data Science** — they complement each other but are distinctly different
- **DE sits UPSTREAM** from data science — DEs provide the inputs that data scientists convert into something useful
- Think: DE = farmer (grows, harvests, cleans, delivers ingredients) / DS = chef (creates dishes from ingredients)

```
    ┌──────────────────┐          ┌──────────────────┐
    │  DATA ENGINEER   │          │  DATA SCIENTIST  │
    │                  │          │                  │
    │  Collects data   │────────▶│  Builds ML models│
    │  Cleans data     │  serves  │  Runs experiments│
    │  Stores data     │  data to │  Makes predictions│
    │  Transforms data │          │  Derives insights│
    │                  │          │                  │
    │   UPSTREAM       │          │   DOWNSTREAM     │
    └──────────────────┘          └──────────────────┘
```

### The Data Science Hierarchy of Needs (Monica Rogati, 2017)

```
              /\
             /  \        ← AI / Deep Learning
            /    \
           / ML   \      ← Machine Learning models
          /________\
         / Analytics\    ← A/B testing, experiments
        /____________\
       / Cleaning &   \  ← Data wrangling, ETL
      / Transformation \
     /_________________\
    /  Data Collection   \  ← Logging, sensors, APIs
   /_____________________\
  / Reliable Data Flow &  \  ← Pipelines, storage,
 /    Storage Infrastructure\   infrastructure
 ‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾

   ★ Data Engineers OWN the bottom 3 layers
   ★ Data Scientists WANT to live at the top
   ★ But spend 70-80% of time in the bottom 3
```

**Key insight:** When DEs build the foundation, data scientists can spend 90%+ of their time on analytics, experimentation, and ML.

### What a DE Does NOT Do
- Does NOT build ML models, create dashboards, perform data analysis, build KPIs, or develop software applications
- But SHOULD understand all these areas to serve stakeholders

---

## Part 2: Data Maturity Model (3 Stages)

```
  Stage 1              Stage 2              Stage 3
  ┌──────────┐        ┌──────────────┐     ┌──────────────┐
  │ STARTING │───────▶│  SCALING     │────▶│  LEADING     │
  │ with data│        │  with data   │     │  with data   │
  └──────────┘        └──────────────┘     └──────────────┘
  Small team           Formal practices     Self-service
  Ad hoc requests      Specialization       Automation
  Generalist DE        Robust architecture  Data as product
  "Move fast"          "Scale smart"        "Lead & govern"
```

### Stage 1: Starting with Data
- **Company:** Fuzzy goals, small data team (single digits), little infrastructure
- **DE Role:** Generalist, plays multiple roles (may also be data scientist/SW engineer)
- **Goal:** Move fast, get traction, add value
- **Focus:** Define initial architecture, get quick wins, build solid foundation, use off-the-shelf tools
- **⚠️ Trap:** Don't jump to ML without a data foundation. Quick wins create tech debt — plan to reduce it. Avoid working in silos.

### Stage 2: Scaling with Data
- **Company:** Formal data practices exist, needs scalable architecture
- **DE Role:** Moving from generalist to specialist
- **Goal:** Scale architecture, adopt DevOps/DataOps, build ML-supporting systems
- **Focus:** Formal practices, scalable architectures, avoid undifferentiated heavy lifting
- **⚠️ Trap:** Don't adopt bleeding-edge tech just because Silicon Valley does. The bottleneck is the TEAM, not the technology. Focus on pragmatic leadership.

### Stage 3: Leading with Data
- **Company:** Truly data-driven, self-service analytics and ML
- **DE Role:** Deep specialist
- **Goal:** Automate, govern, optimize
- **Focus:** Automation for new data sources, custom tools for competitive advantage, data governance & quality, data catalogs & lineage
- **⚠️ Trap:** Complacency — must constantly maintain and improve. Avoid expensive hobby projects that don't deliver business value.

**Key insight:** Data maturity does NOT depend on company age or revenue. A startup can be more data-mature than a 100-year-old company.

---

## Part 3: Skills of a Data Engineer

### Business Skills (Often Neglected!)
1. **Communication** — with both technical and nontechnical people
2. **Requirements gathering** — know what to build, get stakeholder agreement
3. **Cultural understanding** — Agile, DevOps, DataOps are cultural, not just technical
4. **Cost control** — optimize for TCO, time-to-value, opportunity cost
5. **Continuous learning** — field changes fast, filter signal from noise

> "Success or failure is rarely a technology issue."

### Technical Skills — Primary Languages

| Language | Role | Key Tools |
|----------|------|-----------|
| **SQL** | King of data. Queries, transforms, modeling. "Lingua franca of data" | Snowflake, BigQuery, dbt, PostgreSQL |
| **Python** | Bridge between DE and DS. Glue language, APIs, scripting | Airflow, pandas, PySpark, APIs |
| **Java/Scala** | Heavy open-source frameworks, more performant | Spark, Kafka, Flink, Beam |
| **bash** | CLI, OS operations, scripting, automation | awk, sed, cron, orchestration scripts |

**Beginner priority:** SQL + Python → covers 80%+ of DE work.

### The Balancing Act
A DE constantly optimizes across: **Cost, Agility, Scalability, Simplicity, Reuse, Interoperability** — every decision is a trade-off.

---

## Key Takeaways

1. DE sits UPSTREAM from data science — you build the foundation, they build models
2. The Hierarchy of Needs shows why DE matters: without solid bottom layers, AI/ML is impossible
3. Data maturity (3 stages) determines what a DE should focus on
4. Business skills matter as much as technical skills
5. SQL and Python are your two most important starting languages
6. Every DE decision is a trade-off

---

## Comprehension Questions

1. Explain the relationship between DE and data science. Who is upstream?
2. What is the Data Science Hierarchy of Needs? Which layers does a DE own?
3. Name the 3 stages of data maturity. For each: one focus area and one trap.
4. Why does the book say "success or failure is rarely a technology issue"?
5. Which two languages should a new DE learn first, and why?

---

## Practical Exercise

**Scenario:** First DE at a 30-person fintech startup (Stage 1). CEO says: "We have PostgreSQL, Stripe API, and Google Analytics. Our data scientist wants a churn model. What should we do first?"

Write a 5–8 bullet point plan for your first 30 days.

---

## Tool Mapping

| Concept | Real Tool |
|---------|-----------|
| Stage 1: off-the-shelf | Fivetran, BigQuery, Metabase |
| Stage 2: formal practices | dbt, Airflow, Great Expectations |
| Stage 3: governance | DataHub, Monte Carlo, Looker |
| SQL everywhere | Snowflake, BigQuery, dbt, PostgreSQL |
| Python as glue | Airflow DAGs, API connectors, PySpark |

---

*Next: Day 4 — Background & Skills of a DE + Type A vs Type B Engineers*
