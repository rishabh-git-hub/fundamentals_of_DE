# 📘 Day 4: Background & Skills of a DE + Type A vs Type B + DEs Inside Organizations

**Book:** *Fundamentals of Data Engineering* — Chapter 1 (pp. 17–31)  
**Date:** ___________

---

## 🔄 Recap of Day 3

DE sits upstream from data science. Data Science Hierarchy of Needs — DEs own bottom 3 layers. Data Maturity Model: Starting → Scaling → Leading. Business + technical skills both matter. SQL + Python are primary languages.

---

## Part 1: Career Paths into Data Engineering

- **No formalized path** — no standard university curriculum
- Easiest transitions from: Software Engineering, ETL Development, Database Admin, Data Science, Data Analysis
- Everyone must invest in **self-study**
- **Key advice:** Focus on fundamentals (what won't change) + monitor developments (where field is going)

---

## Part 2: Type A vs Type B Data Engineers

### Type A = Abstraction
- Avoids undifferentiated heavy lifting
- Uses off-the-shelf products, managed services, tools
- Works at companies across ALL maturity stages
- Example: Using Fivetran + Snowflake + dbt + Looker

### Type B = Build
- Builds custom data tools and systems
- Leverages company's core competency and competitive advantage
- More common at Stage 2 & 3 companies
- Example: Netflix building custom data platform

### Key Points
- Type A and B can be the **same person** at the same company
- Type A is typically hired first to set the foundation
- Type B skills learned or hired as needs arise
- **Beginner advice:** Start as Type A. Type B comes naturally with experience.

```
 TYPE A (Abstraction)         TYPE B (Build)
 ────────────────────         ────────────────
 Managed services             Custom systems
 Off-the-shelf tools          Internal platforms
 All maturity stages          Stage 2 & 3
 Faster time to value         Competitive advantage
 Lower maintenance            Higher control
```

---

## Part 3: Internal-Facing vs External-Facing DEs

### External-Facing
- Serves users of external apps (social media, IoT, e-commerce)
- Higher concurrency loads
- More complex security (multi-tenant data)
- Feedback loop: app → data pipeline → back to app
- Example: Spotify Wrapped, Amazon recommendations

### Internal-Facing
- Serves business and internal stakeholders
- BI dashboards, reports, data science, ML models
- Moderate load, simpler security
- Example: Sales dashboard in Tableau for leadership

**In practice:** Internal-facing data is usually a prerequisite to external-facing. Most DEs start internal-facing.

---

## Part 4: The Stakeholder Map

```
         UPSTREAM (produce data)
  ┌────────────────────────────────┐
  │ Data Architects                │
  │ Software Engineers             │
  │ DevOps / SREs                  │
  └───────────────┬────────────────┘
                  ▼
         ┌─────────────────┐
         │  DATA ENGINEER  │
         └────────┬────────┘
                  ▼
  ┌────────────────────────────────┐
  │ Data Analysts                  │
  │ Data Scientists                │
  │ ML Engineers                   │
  │ Business Users                 │
  └────────────────────────────────┘
         DOWNSTREAM (consume data)
```

### Upstream Roles
- **Data Architects** — Design blueprints for data management, bridge between technical and nontechnical sides
- **Software Engineers** — Build apps that generate data (events, logs). Critical to coordinate with them on schema, volume, format
- **DevOps/SREs** — Produce operational monitoring data. Both upstream and downstream

### Downstream Roles
- **Data Scientists** — Build prediction models. Need clean, reliable, timely data
- **Data Analysts** — Interpret data, create reports/dashboards. Need well-structured, queryable data
- **ML Engineers** — Deploy models to production. Need reliable feature-serving pipelines

---

## Part 5: Data Engineers and Business Leadership

### C-Suite Roles
| Role | Focus | Relationship with DE |
|------|-------|---------------------|
| **CEO** | Company vision | Wants to know what's possible with data |
| **CIO** | Internal IT strategy | Collaborates on cloud migrations, data systems |
| **CTO** | External tech strategy | Owns app architecture, critical data sources |
| **CDO** | Data assets & strategy | Oversees data products, governance, privacy |
| **CAO** | Analytics & decisions | May oversee data science and ML |

### Working with Managers
- **Project Managers** — Direct sprints, filter requests, prioritize deliverables (Agile/Scrum)
- **Product Managers** — Own data products, balance tech vs. customer needs

### Key Quote
> "Companies don't hire engineers simply to hack on code in isolation. Engineers should develop a deep understanding of the problems they're tasked with solving, the tools at their disposal, and the people they work with and serve."

---

## Part 6: Evaluating New Tools/Trends

When you hear about a new tool, ask:
1. Which lifecycle stage does it address?
2. What undercurrent does it improve?
3. Does it solve a real problem I have, or is it hype?
4. What's the TCO vs. what I already use?
5. Is this immutable (will last) or transitory (might fade)?

---

## Chapter 1 Summary (Days 1–4)

| Day | What You Learned |
|-----|-----------------|
| Day 1 | WHAT is DE + The Lifecycle (5 stages + 6 undercurrents) |
| Day 2 | WHERE it came from (4 eras of history) |
| Day 3 | WHY it matters (DE vs DS, Hierarchy of Needs, Maturity, Skills) |
| Day 4 | WHO does it and HOW (Type A/B, stakeholders, career paths) |

---

## Comprehension Questions

1. Difference between Type A and Type B DE? When is each the right fit?
2. Name 3 upstream and 3 downstream stakeholders. Why does direction matter?
3. Internal-facing vs external-facing DE? Which has higher security complexity?
4. What does a CDO do and how does it relate to DE?
5. Why is "focus on fundamentals, monitor developments" better than chasing every new tool?

---

## Practical Exercise

Look at 3 real DE job postings. For each, identify:
1. Type A or Type B role?
2. What data maturity stage is this company in?
3. Internal-facing or external-facing?
4. Who are the likely upstream/downstream stakeholders?

---

## Tool Mapping

| Concept | Real-World Example |
|---------|-------------------|
| Type A | Fivetran + Snowflake + dbt + Looker |
| Type B | Netflix/Uber building custom platforms |
| Internal-facing | Snowflake → Tableau dashboards for sales |
| External-facing | Pipeline powering Spotify Wrapped |
| DE ↔ SW Eng | Coordinating schema changes |
| DE ↔ Data Scientist | Building feature pipelines |

---

*Next: Day 5 — DEs Inside Organizations (deep dive) + Working with all roles + Chapter 1 conclusion*
