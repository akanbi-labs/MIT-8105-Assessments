# Olaham Academy — Advanced Database Systems Portfolio

**Course:** MIT 8103 — Advanced Database Systems  
**Assessment:** Individual Practical Database Portfolio (40 marks)  
**Case study:** Proposed Training and Learner Management System for Olaham Academy  
**Student:** Hamid Akanbi   
**Email:** h.akanbi9301@miva.edu.ng  
**Academic session:** 2026/2027

## Overview

This repository contains practical evidence and documentation for five database portfolio activities based on a **proposed** Olaham Academy learner-management system. The exercises use fictional participant records, not private data from the organisation.

## Portfolio contents

| Folder | Activity | Evidence |
| `Portfolio-1-Database-Design/` | Database Design and Modelling | PostgreSQL schema, ER diagram, sample records, constraints, normalisation and README |
| `Portfolio-2-Query-Optimisation/` | Query Processing and Optimisation | SQL queries, 100,000 synthetic benchmark events, execution plans, index and performance analysis |
| `Portfolio-3-Transactions-Concurrency/` | Transactions and Concurrency | COMMIT, ROLLBACK, isolation and row-locking demonstrations, screenshots and README |
| `Portfolio-4-NoSQL/` | NoSQL and Advanced Data Models | MongoDB documents, query examples, model suitability analysis, screenshots and README |
| `Portfolio-5-Distributed-Cloud/` | Distributed and Cloud Database Exercise | Local MongoDB configuration checks, proposed cloud/replica-set architecture, technical analysis and README |

Each folder contains its own instructions and supporting evidence. Some filenames may differ slightly; use the actual names saved in the repository.

## Technology

- PostgreSQL 18 and pgAdmin 4 for the relational database, SQL queries and transaction tests.
- MongoDB Community Server and Compass/mongosh for document-oriented modelling and local deployment inspection.
- GitHub for versioned evidence and technical documentation.

## Selected results

- **Relational model:** Eight core tables representing programmes, cohorts, participants, facilitators, enrolments, sessions, assessments and submissions.
- **SQL optimisation:** On one recorded benchmark run, execution time changed from **25.981 ms** (sequential scan) to **0.221 ms** (index-only scan) using the composite index `idx_activity_type_time` on `portfolio2_activity_log(event_type, event_time)`. This is a single-run comparison; repeated measurements are needed for a reliable average.
- **Transactions:** COMMIT and ROLLBACK were tested; a two-connection concurrency demonstration reduced the test table's available slots from 10 to 8, with locking observed.
- **NoSQL:** A `student_portfolios` document collection demonstrated arrays, embedded project records and filtering by completion status, skills and score.
- **Distributed/cloud exercise:** The tested MongoDB deployment ran on `localhost:27017` as a standalone server. Replica sets, sharding and cloud deployment are **proposed and discussed**, not represented as implemented.

## Reproduction and evidence

Read each portfolio's `README.md` before running its scripts. The SQL scripts contain statements that create tables, insert records and deliberately trigger errors; **do not rerun them wholesale against an already populated database**. Execute selected sections on a disposable/test database where appropriate. The Portfolio 4 `.js` script is intended for `mongosh`.

Screenshots and output files document the operations performed. No passwords or private organisational datasets should be included.

## Final report and submission

The lecturer requires a **2–3 page final documentation report uploaded to the LMS**, including the case study, all five portfolio activities, a working GitHub link, screenshots/evidence, individual technical reflection, references and an AI-use declaration where applicable. The final Word/PDF report is a **separate LMS submission**; this repository-level README is its navigation page, not a substitute for that report.

**GitHub repository URL:** https://github.com/akanbi-labs
**Assessor access:** Open 



## References 
- PostgreSQL documentation: https://www.postgresql.org/docs/
- MongoDB documentation: https://www.mongodb.com/docs/
- Course assessment brief: *MIT 8103 Advanced Database Systems, 2026/2027 First Semester Continuous Assessment*.

