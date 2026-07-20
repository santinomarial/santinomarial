# Hi, I'm Santino Marial 👋

**Software Engineer · CS & Statistics @ Harvard ('27)**

I build backend systems, ML pipelines, and AI infrastructure — from a C++ database engine written from scratch to real-time anomaly detection pipelines processing 10,000+ alerts a day. I care about performance, reliability, and shipping things people actually use.

📍 Cambridge, MA  📫 smarial@college.harvard.edu

<a href="https://linkedin.com/in/santinomarial"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="https://github.com/santinomarial"><img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white" alt="GitHub"/></a>
<a href="mailto:smarial@college.harvard.edu"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" alt="Email"/></a>

---

## Tech Stack

**Languages**
![C++](https://img.shields.io/badge/-C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/-Java-007396?style=flat&logo=openjdk&logoColor=white)
![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

**Backend & Data**
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/-Flask-000000?style=flat&logo=flask&logoColor=white)
![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat&logo=node.js&logoColor=white)
![NestJS](https://img.shields.io/badge/-NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)
![GraphQL](https://img.shields.io/badge/-GraphQL-E10098?style=flat&logo=graphql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/-Redis-DC382D?style=flat&logo=redis&logoColor=white)

**ML & Infra**
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/-scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![DSPy](https://img.shields.io/badge/-DSPy-black?style=flat)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat&logo=react&logoColor=black)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=flat&logo=git&logoColor=white)

---

## Featured Projects

**[Meridian](https://github.com/santinomarial/Meridian)** — CRDT-based collaborative IDE
- Multi-client edits needed to merge without conflicts, so I used **Yjs** as the CRDT layer, with **Socket.IO** managing document rooms to route real-time sync across clients and **Monaco** providing the in-browser editor surface.
- Sessions needed to survive restarts without replaying the full edit history, so I designed an append-only update log in **PostgreSQL** with periodic snapshot compaction, enabling fast cold-start reconstruction and low-latency state recovery.
- Built the client in **TypeScript/React** and the server in **NestJS**, with **Redis** backing pub/sub across service instances.

**[Collaborative Code Editor](https://github.com/santinomarial/collaborative)** — Real-time multi-user editor
- Needed conflict-free concurrent edits across 30+ users, so I built a custom Operational Transformation engine to resolve conflicting changes in real time, hitting sub-150ms sync.
- To scale sync across many concurrent sessions, I used **WebSockets** for the live connection layer with **Redis** pub/sub to broadcast edits horizontally across server instances.
- Built the frontend in **React** and backend in **Node.js**, with **MongoDB** persisting document state; adopted by 25 Harvard CS students.

**[Forward Repair for RAG Pipelines](https://github.com/santinomarial/forward-repair-lm-pipelines)** — RAG pipeline repair framework
- Needed to isolate *where* in a multi-stage RAG pipeline failures originate, so I built the framework on **DSPy** to programmatically corrupt and repair individual pipeline stages.
- Compared query-stage vs. answer-stage failures specifically, using **HotpotQA** as the benchmark dataset with **BM25** retrieval to ground each experiment.
- Implemented entirely in **Python**, structured so each pipeline stage could be corrupted/repaired independently for controlled comparison.

---

## Experience

**Software Engineer, ML** — Harvard Undergraduate Machine Learning Club *(Jan 2026 – May 2026)*
- Synchronous inference calls were the main latency bottleneck in the generation pipeline, so I re-architected it around async **FastAPI** workers and task queuing to parallelize multi-stage inference, cutting per-video turnaround to sub-90s.
- Repeated calls on similar inputs were driving up API spend, so I introduced a **Redis**-backed caching layer in front of the model calls, reducing costs by 35% while sustaining 99%+ uptime for 50+ students.
- Owned the backend end-to-end — queue architecture, caching strategy, and deployment — turning a research prototype into a production service the club now runs on weekly.

**Software Engineer, AI** — Harvard Grid *(Sep 2025 – Dec 2025)*
- Security alerts were arriving faster than analysts could triage manually, so I built and deployed a real-time anomaly detection pipeline on **AWS** (Python) handling 10,000+ daily alerts at sub-3s latency, for under $100/month in cloud costs.
- False positives were burying real signal, so I trained **scikit-learn** models on engineered **Pandas/NumPy** feature pipelines, pushing precision past 80% and cutting false positives by 60%.
- Balanced model complexity against infrastructure cost at every stage, proving high-throughput detection didn't require a high cloud bill.

**Software Engineer Intern** — MoMo from MTN *(May 2025 – Aug 2025)*
- Manual reconciliation across 50K+ daily transactions was slow and error-prone, so I built a backend service using **REST APIs** and **SQL**-based status checks to automate matching, cutting reconciliation time by 35%.
- To catch failed, delayed, and mismatched payments before they hit settlement, I layered custom matching, validation, and exception-reporting logic on top of the core service.
- This lifted reconciliation accuracy to 99%+ across daily settlement workflows, directly reducing operational risk on high-volume payment flows.

**Engineering & Research Intern** — diiVe, Cape Town *(Jun 2024 – Aug 2024)*
- Raw labor records arrived messy and unstructured, so I built **Python** data pipelines to clean and transform them into analysis-ready datasets.
- These pipelines fed directly into client-facing deliverables, turning raw data into insights that shaped slides and policy recommendations for stakeholders.
- Worked at the intersection of engineering and research, making sure the data foundation was solid enough to support decisions made downstream by non-technical stakeholders.

**Program Coordinator & Engineer** — Young Leaders Academy of South Sudan *(Sep 2023 – Present)*
- The academy needed a central platform to support onboarding, content access, and program operations, so I built and maintained a full-stack learning platform using **React**, **Node.js**, **TypeScript**, **GraphQL**, and **MongoDB**.
- Split time between engineering the platform and coordinating the program itself, keeping the tool aligned with how staff and students actually used it day to day.
- Sustained this dual technical and coordination role for 3+ years alongside a full-time Harvard course load, reflecting a long-term commitment to the organization's mission.
