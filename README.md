# Google Fiber Customer Service Dashboard - BI Project

<img src="Images/Readme_dashboard_mockup.jpg" alt="DB Mockup" height="300px">

<br>

![Project Status](https://img.shields.io/badge/Status-Data%20Preparation-yellow)
![Phase](https://img.shields.io/badge/Phase-2%20of%203-blue)

## Project Overview

Business intelligence dashboard for Google Fiber's customer service team analysing repeat caller patterns and improving first-call resolution rates across three market cities.

### Business Problem

The team needs to understand how often customers call support again after their first inquiry. This will help leaders assess whether the team answers customer questions the first time. Leaders want to explore trends in repeat calls to identify why customers call more than once and how to improve the overall customer experience.

### Success Criteria

The team's goal is to reduce call volume by increasing customer satisfaction and improving operations. The dashboard should demonstrate an understanding of this goal and provide stakeholders with insights about repeat caller volumes in different markets and the types of problems they represent.

---

<br>

### Phase 1: Planning

**Tasks:**
- [x] Stakeholder Requirements Document
- [x] Stakeholder Follow-up Questions
- [x] Project Requirements Document
- [x] Strategy Document
- [x] Milestone Plan

### Key Stakeholders

| Name | Role |
|------|------|
| Emma Santiago | Hiring Manager |
| Keith Portone | Project Manager |
| Minna Rah | Lead BI Analyst |
| Ian Ortega | BI Analyst |
| Sylvie Essa | BI Analyst |

*Primary contacts: Emma Santiago and Keith Portone*

### Available Datasets

This fictional dataset is a version of actual data the team works with. The data is anonymised and approved.

**Data includes:**
- Number of calls
- Number of repeat calls after first contact
- Call type
- Market city
- Date

**Market cities:**
- market_1
- market_2
- market_3

**Problem types:**
- Type_1: Account management
- Type_2: Technician troubleshooting
- Type_3: Scheduling
- Type_4: Construction
- Type_5: Internet and WiFi

**Repeat call tracking:**
- Initial contact date listed as `contacts_n`
- Subsequent calls listed as `contacts_n_[number of days since first call]`
- Example: `contacts_n_6` indicates six days since first contact
- Dataset records repeat calls over seven-day periods

### Project Goals

**Primary Questions:**
1. How often does the customer service team receive repeat calls from customers?
2. What problem types generate the most repeat calls?
3. Which market city's customer service team receives the most repeat calls?

**Required Deliverables:**
- A chart or table measuring repeat calls by their first contact date
- A chart or table exploring repeat calls by market and problem type
- Charts showcasing repeat calls by week, month, and quarter

### Dashboard Access

People with dashboard-viewing privileges:
- Emma Santiago
- Keith Portone
- Minna Rah
- Ian Ortega
- Sylvie Essa

### Accessibility Requirements

Per Minna Rah's requirements, all dashboards must include:
- Large print options
- Text-to-speech alternatives
- Colour-blind friendly visualisations

### Project Approvals and Dependencies

Stakeholders must have access to all datasets so they can explore the steps taken during the project.

---

<br>

## Timeline

**Phase 1: Planning** (Completed)
- Document stakeholder requirements
- Define project scope and strategy
- Create milestone plan

**Phase 2: Data Preparation** (Current)
- Assess data integrity and quality
- Build ETL pipelines
- Document data limitations

**Phase 3: Dashboard Design** (Upcoming)
- Design dashboard mockups
- Build interactive dashboard
- Implement monitoring and iteration processes

---

<br>

## Contact

This is a course project demonstrating end-to-end BI development process for portfolio purposes.

**Last Updated:** 22/02/25
