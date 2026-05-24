<img src="../00_Resources/Phase2_Banner.png" alt="phase1_banner">

![Project Status](https://img.shields.io/badge/Status-In%20Progress-blue)

Phase 1 produced the planning documents — stakeholder needs, KPIs, and expectations. Phase 2 is about taking raw data and shaping it into a clean reporting table that the dashboard in Phase 3 will sit on top of. Get this wrong and the dashboard is built on sand.

---

<br>

## Tasks

- [ ] Understand the source data — tables, contents, and grain of each  
- [ ] Upload data to BigQuery — create project space and load the three market datasets  
- [ ] Identify joins and transformations — table relationships, cleaning, filtering, and derived fields required  
- [ ] Write the SQL — combine into a single reporting table via BigQuery  
- [ ] Validate the output — does the reporting table answer the stakeholder questions from Phase 1?

---

<br>

## Source Data Exploration

*To be completed once data has been reviewed.*

| Dataset | Description | Row Count | Date Range |
|---------|-------------|-----------|------------|
| market_1 | TBC | TBC | TBC |
| market_2 | TBC | TBC | TBC |
| market_3 | TBC | TBC | TBC |

**Table grain:** One row per market / date / problem type.

---

<br>

## Data Schema & Table Relationships

All three market tables share an identical schema — combined via `UNION ALL`.

```
market_1 ─┐
           ├──► UNION ALL ──► reporting_table
market_2 ─┤
market_3 ─┘
```

---

<br>

## BigQuery: Reporting Table

**SQL**

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

**Validation Checklist**

- [ ] Data present from all three markets  
- [ ] All five problem types represented  
- [ ] Row count matches sum of source tables  
- [ ] No nulls introduced by the union  
- [ ] Reporting table answers the three core stakeholder questions from Phase 1  

---

<br>

[← Back to Main README](https://github.com/DataDaneHQ/google-fiber-bi-dashboard/blob/main/README.md)