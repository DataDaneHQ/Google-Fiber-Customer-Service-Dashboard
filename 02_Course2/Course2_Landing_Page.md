<img src="../00_Resources/Phase2_Banner.png" alt="phase1_banner">

<br>

## Phase 2: Data Preparation

Phase 1 produced the planning documents — stakeholder needs, KPIs, and expectations. Phase 2 is about taking raw data and shaping it into a clean reporting table that the dashboard (Phase 3) will sit on top of. Get this wrong and the dashboard is built on sand, so it's worth being methodical.

**Tasks:**  
- [ ] **Understand the source data** — What tables do we have? What do they contain? What is the grain of each table?  
- [ ] **Upload data to BigQuery** — Create a project space and upload the three market datasets ready for querying.  
- [ ] **Identify joins and transformations** — How do the tables relate? What cleaning, filtering, or derived fields are needed?  
- [ ] **Write the SQL** — Combine everything into a single reporting table via BigQuery.  
- [ ] **Validate the output** — Does the reporting table answer the stakeholder questions established in Phase 1?  

---

<br>

## Source Data Exploration  

_This section will document findings from initial exploration of the three market
datasets. To be completed once data has been reviewed._


### Dataset Overview

| Dataset | Description | Row Count | Date Range |
|---------|-------------|-----------|------------|
| market_1 | _TBC_ | _TBC_ | _TBC_ |
| market_2 | _TBC_ | _TBC_ | _TBC_ |
| market_3 | _TBC_ | _TBC_ | _TBC_ |

### Table Grain

One row per market / date / problem type.

---

<br>


## Data Schema & Table Relationships

```
market_1 ─┐
           ├──► UNION ALL ──► reporting_table
market_2 ─┤
market_3 ─┘
```

All three tables share an identical schema. Combined via `UNION ALL` — same structure,
different markets.

---

<br>

## BigQuery: Reporting Table

### SQL

```sql
SELECT
    'market_1' AS market,
    date,
    problem_type,
    contacts_n,
    contacts_n_1,
    contacts_n_2,
    contacts_n_3,
    contacts_n_4,
    contacts_n_5,
    contacts_n_6
FROM market_1

UNION ALL

SELECT
    'market_2' AS market,
    date,
    problem_type,
    contacts_n,
    contacts_n_1,
    contacts_n_2,
    contacts_n_3,
    contacts_n_4,
    contacts_n_5,
    contacts_n_6
FROM market_2

UNION ALL

SELECT
    'market_3' AS market,
    date,
    problem_type,
    contacts_n,
    contacts_n_1,
    contacts_n_2,
    contacts_n_3,
    contacts_n_4,
    contacts_n_5,
    contacts_n_6
FROM market_3;
```

### Validation

- [ ] Data present from all three markets
- [ ] All five problem types represented
- [ ] Row count matches sum of source tables
- [ ] No nulls introduced by the union
- [ ] Reporting table answers the three core stakeholder questions from Phase 1

<br>