# Santino Marial

**Software Engineer · Backend Systems, ML Infrastructure & Applied AI**  
Computer Science & Statistics at Harvard University · Class of 2027

I build production systems for data-intensive and operationally critical workflows. Across security, machine learning, payments, and education, I have owned software from architecture and implementation through deployment and optimization, with a focus on reliability, performance, and measurable impact.

Cambridge, MA

<a href="https://linkedin.com/in/santinomarial"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="mailto:smarial@college.harvard.edu"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" alt="Email"/></a>

---

## Technical Skills

**Languages**  
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

**Backend, APIs & Databases**  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat&logo=graphql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)

**Machine Learning & AI**  
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![DSPy](https://img.shields.io/badge/DSPy-000000?style=flat)

**Frontend, Cloud & Tooling**  
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

---

## Selected Projects

### [Meridian](https://github.com/santinomarial/Meridian) — Durable CRDT Collaboration Platform

- Engineered a real-time collaborative IDE using **Yjs**, **Socket.IO**, and **Monaco**, enabling conflict-free document editing across multiple clients.
- Designed a durable **PostgreSQL** state layer using an append-only update log and periodic snapshot compaction, supporting fast recovery without replaying complete document histories.
- Built the **React/TypeScript** client and **NestJS** backend, with **Redis pub/sub** coordinating updates across service instances.

### [Collaborative Code Editor](https://github.com/santinomarial/collaborative) — Custom Operational Transformation Engine

- Implemented an **Operational Transformation** engine from first principles, supporting more than 30 concurrent users with synchronization latency below 150 milliseconds.
- Built a **WebSocket** synchronization layer with **Redis pub/sub** to distribute edits across **Node.js** server instances.
- Developed the **React/Node.js/MongoDB** application, which was used by 25 Harvard computer science students.

### [Forward Repair for RAG Pipelines](https://github.com/santinomarial/forward-repair-lm-pipelines) — RAG Reliability Framework

- Architected a **Python/DSPy** framework that injects, isolates, and repairs query- or answer-stage RAG failures without rerunning unaffected stages.
- Demonstrated across **300 HotpotQA examples** that query repair improved exact match by **19.3 percentage points**, while answer repair recovered only **2.2%** of failures.
- Engineered interchangeable **BM25/dense retrieval** and **OpenAI/Ollama** backends with cost and latency telemetry, **36 deterministic tests**, **92% targeted coverage**, and automated CI.

---

## Experience

### Software Engineer, Machine Learning — Harvard Undergraduate Machine Learning Club

*January 2026 – May 2026*

- Re-architected a synchronous generation pipeline as an asynchronous **FastAPI** worker system with task queues, parallelizing multi-stage inference and reducing per-video turnaround to under 90 seconds.
- Implemented a **Redis-backed caching layer** for reusable model responses, reducing API costs by 35% while supporting weekly use by more than 50 students.
- Owned backend architecture, caching strategy, and deployment, transforming a research prototype into a production service used by the club each week.

### Software Engineer, AI — Harvard Grid

*September 2025 – December 2025*

- Built and deployed a real-time anomaly detection pipeline on **AWS** using **Python**, processing more than 10,000 security alerts daily with under three-second latency and less than $100 per month in cloud costs.
- Engineered **Pandas/NumPy** feature pipelines and trained **scikit-learn** models, achieving over 80% precision while reducing false positives by 60%.

### Software Engineer Intern — MoMo from MTN

*May 2025 – August 2025*

- Developed a backend reconciliation service using **REST API integrations** and **SQL-based status checks**, automating matching across more than 50,000 daily transactions and reducing reconciliation time by 35%.
- Implemented custom matching, validation, and exception-reporting logic to identify failed, delayed, and mismatched payments before settlement.
- Increased reconciliation accuracy to over 99%, reducing operational risk across high-volume payment settlement workflows.

### Engineering & Research Intern — diiVe

*June 2024 – August 2024 · Cape Town, South Africa*

- Developed **Python** data pipelines to clean, standardize, and transform unstructured labor records into analysis-ready datasets.
- Produced reliable datasets that supported client-facing analysis, stakeholder presentations, and policy recommendations.

---

## Leadership & Community

### Program Coordinator & Engineer — Young Leaders Academy of South Sudan

*September 2023 – Present*

- Build and maintain a full-stack learning platform supporting student onboarding, content delivery, and program operations using **React**, **Node.js**, **TypeScript**, **GraphQL**, and **MongoDB**.
- Translate staff and student workflows into product improvements while coordinating the academy’s day-to-day program operations.
