<div align="center">

<img src="banner.png" alt="Brijesh Kumar — Agentic AI Engineer" width="100%" />

# Hi, I'm Brijesh Kumar 👋

### Agentic AI Engineer — I build agents that are *allowed to act*, and the evaluation that makes that safe

**M.S. Computer Science @ Arizona State University · 4.0 / 4.0 · Graduating December 2026**

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=21&pause=1100&color=3178C6&center=true&vCenter=true&width=940&lines=Agentic+AI+Engineer+%40+EdPlus%2C+Arizona+State+University;MCP+gateways+%7C+LangGraph+supervisors+%7C+ReAct+tool+calling;RAG+with+grounding+checks%2C+not+just+retrieval;Evaluation+harnesses%2C+approval+gates%2C+audit+trails;Three+years+of+backend+and+platform+underneath+it;Open+to+full-time+roles+from+December+2026" alt="What I do" />

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-171717?style=for-the-badge&logo=vercel&logoColor=white)](https://brijeshbuilds.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge)](https://linkedin.com/in/brijeshkumar03)
[![Email](https://img.shields.io/badge/Email-C5221F?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kumarbrijesh.dev@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-2EA043?style=for-the-badge&logo=readdotcv&logoColor=white)](https://brijeshbuilds.com/resume/Brijesh_Kumar_Resume.pdf)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Brijesh03032001)

<br/>

![Agent tool-call success](https://img.shields.io/badge/Agent_tool--call_success-97.2%25-3178C6?style=flat-square)
![Golden-set agreement](https://img.shields.io/badge/Golden--set_agreement-89%25-3178C6?style=flat-square)
![Unauthorized agent actions](https://img.shields.io/badge/Unauthorized_agent_actions-zero_in_prod-2EA043?style=flat-square)
![Unsupported claims](https://img.shields.io/badge/Unsupported_claims-down_35%25_vs_baseline-3178C6?style=flat-square)
![Springer](https://img.shields.io/badge/Springer-sole--author_publication-C44F00?style=flat-square)
![Y Combinator](https://img.shields.io/badge/Y_Combinator-Startup_School_2026-C44F00?style=flat-square)

</div>

---

> [!IMPORTANT]
> **Open to full-time Agentic AI / AI Engineering roles from December 2026.**
> Authorized to work in the U.S. on OPT · based in Tempe, AZ for my final semester, most weeks in San Francisco, happy to relocate.
> Right now I'm building MCP tool gateways and agent evaluation harnesses at **EdPlus**, and grounded clinical RAG at **ASU Biodesign**.

---

## 🧠 What I actually build

Anyone can call an LLM. The hard part is letting one **take an action** — delete a video, place an order, run a shell command, answer a clinical question — and still be able to prove afterwards that it was the right one. That's the problem I work on.

| Agent | The hard part | Result |
|---|---|---|
| **[SlackAgent](https://github.com/Brijesh03032001/SlackAgent)** — acts across Slack, GitHub and Notion | Making 59 tools from three different schema dialects usable by one agent, and keeping it answering when a dependency dies | **97.2%** tool success across 100+ concurrent test conversations, 3 fallback layers, work queued instead of dropped on a 403 |
| **[Aria](https://github.com/Brijesh03032001/Aria)** — voice assistant that drives a Mac | Letting a blind user run shell commands and checkouts by voice without it ever being dangerous | **5 agents** behind a LangGraph supervisor at **under 1 s**, 3 high-risk classes gated on spoken confirmation, 4 PII types scanned before typing |
| **[FoodPilot AI](https://github.com/Brijesh03032001/foodai)** — ReAct copilot over sales and reviews | Stopping an LLM from confidently ordering options that don't exist | Every generated line checked against **2,622** seeded modifiers, applied or rejected **with a reason**, human confirms |
| **[TrustMed-AI](https://github.com/Brijesh03032001/TrustmedAi)** — medical RAG you can audit | Proving a medical answer came from its sources, not the model's memory | **9K+** chunks, 3 domain-routed collections, cross-encoder reranking, a **100-prompt** eval suite with a visible ReAct trace |
| **[Ghosty](https://github.com/Brijesh03032001/Ghosty_A_Conference_helper)** — voice memo to drafted follow-up | Capture that still works when conference Wi-Fi doesn't | 🏆 **Winner, Kiro Spark Challenge 2026** · offline-first queue recovered **100% of 30** simulated drops |

---

## ⚙️ How I build agents that are allowed to act

| Layer | What I actually do | Where it shipped |
|---|---|---|
| **Orchestration** | A supervisor routes to narrow, specialized agents instead of one prompt that does everything. I write the tool loop by hand first, then reach for the framework. | Aria · FoodPilot · EdPlus |
| **Tool interfaces** | **MCP** gateways with schema validation and auth behind one interface, converting external schemas so an agent works across apps it was never built for. | EdPlus (8 tools) · SlackAgent (59) |
| **Retrieval** | Domain-routed collections, optional FAISS refinement, cross-encoder reranking — never one generic vector bucket. | TrustMed-AI · Biodesign · EdPlus |
| **Memory** | Long-term facts kept separately from conversation history, and visible to the user, who can add or delete them. | SlackAgent (mem0) |
| **Evaluation** | Golden sets, grounding checks, Precision@K and MRR harnesses. A failed grounding evaluation **blocks the release**. | EdPlus (89%) · Biodesign · TrustMed-AI |
| **Guardrails** | Approval gates before destructive actions, PII scans before typing, confidence thresholds routing exceptions to a human. | EdPlus · Aria · Biodesign |
| **When it breaks** | Fallback ladders, work queued on rate limits rather than dropped, dead-letter queues, audit trails you can replay. | SlackAgent · Aria · Nexus |

That last row is why three years of backend, payments and Kubernetes work sits below — **agents fail like distributed systems, so I treat them that way.**

---

## 💼 Experience

### 🤖 EdPlus at Arizona State University — AI Software Engineer
`Sep 2025 – Present · Tempe, AZ`

- Built an **MCP gateway** exposing 8 video-editing and job-status tools behind one authenticated interface with schema validation, cutting integration time for new agent tools from **6 hours to 2** and holding **zero unauthorized executions** across 100+ adversarial tests.
- Cut lecture-search query time **25%** by separating retrieval, scoring and synthesis into **LangChain** sub-agents over 10,000+ **pgvector** embeddings, returning the exact timestamp in under 3 seconds.
- Engineered an evaluation harness scoring **ReAct** cut, keep and review labels against 300+ hand-labelled video chunks at **89% agreement** with human labels, behind a mandatory editor approval gate that kept unauthorized production deletions at zero.
- Deployed the backend with Docker on AWS **ECS Fargate** and embedded **Bedrock** summarization with cut/keep/review recommendations in the editor timeline, cutting average session review time **35%** — from 40 minutes to 26.
- Shipped 15+ async **FastAPI** endpoints processing 10+ segments concurrently at **p95 under 3 seconds**, and streamlined Next.js state with Redux, cutting QA-reported state bugs 45%.

### 🔬 ASU Biodesign Institute — Machine Learning Researcher
`Feb 2025 – Present · Tempe, AZ`

- Automated healthcare document intake with a **tool-calling** service for invoice extraction, insurance classification and retrieval. Schema validation and confidence thresholds cut manual work **~30%** and routed **100%** of high-risk exceptions to human review.
- Rolled out the clinician **RAG** app to **4 external clinics** after on-site discovery, configuring PDF retrieval over approved documents behind sign-in. Average case review fell from **15 minutes to 5** for 60+ clinicians.
- Fine-tuned a pretrained **LLM** for clinical summarization, tokenizing documents and reference summaries with its subword tokenizer and chunking inputs to the context window. Reported accuracy rose **28%** over the base model.
- Designed a **FAISS** vector-search RAG pipeline over clinical, metagenomic and literature embeddings, benchmarking 3 embedding approaches and adopting the strongest — retrieval F1 up **22%**, biomarker-discovery precision up **21%** across 3 research domains.
- Grounded clinical research Q&A in its sources, cutting unsupported claims **35%** against an ungrounded baseline. A failed grounding evaluation blocked the release until flagged answers were remediated and a reviewer approved them.

### ⚡ AWL Metaverse Pvt. Ltd. — Software Engineer
`Mar 2024 – Dec 2024 · India`

- Carried **10,000+ concurrent connections** at sub-100 ms on JWT-authenticated **Go WebSockets** after a polling loop collapsed under peak load, tuning **Kubernetes** HPA policies and cutting delivery latency 60% with about 45% less redundant traffic.
- Traced incidents to unindexed queries and exhausted connections in Java **Spring Boot** services, reworking **PostgreSQL** indexing, SQL query optimization and JDBC connection pooling to lift query performance 40%, cut incidents 50% and troubleshooting time 35%.
- Stopped pods dying under resource contention on Amazon **EKS** with CPU and memory requests and limits, Helm-managed rollouts and health probes, with HPA absorbing load — about **35% fewer resource failures** at 99.9% availability.
- Cut mean recovery time about **30%** across Dockerized microservices by building a diagnosis path for pod failures, CrashLoopBackOff events and resource exhaustion from container logs and **Prometheus** monitoring.
- Rewrote a JavaScript rendering prototype too slow for 4K scrubbing as a **C++** engine compiled to **WebAssembly** and embedded in the React instructor dashboard, cutting frame-scrubbing latency **65%** for 30+ instructors.

### 💳 Quicket Solutions — Software Developer *(promoted from Intern)*
`Software Developer: Mar 2023 – Mar 2024 · Intern: Oct 2022 – Feb 2023 · India`

- Strengthened high-traffic Java **Spring Boot** payment APIs with **Redis** caching that cut database load **60%** during traffic spikes, then contained failures with circuit breakers, bounded retries and graceful degradation that 3 engineering teams adopted.
- Resolved duplicate charges after network timeouts with 3 safeguards — **Stripe** idempotency keys, webhook deduplication and **PostgreSQL** uniqueness constraints — then added audit logging to trace discrepancies between payment records and the ledger.
- Engineered 20+ reusable React and **Next.js** components for the payments module and centralized their shared state in **Redux**, cutting duplicated state logic about 30% across the payment workflows.
- Wired **Stripe** payment APIs into 5+ checkout scenarios end to end, covering payment initiation, transaction-status handling and distinct success and failure experiences, cutting frontend integration effort about 25%.
- Hardened critical payment workflows with JUnit, Mockito and **Jest** unit and integration tests to **80% coverage**, supporting 2 newer engineers through code reviews and pair programming. Awarded **Best Intern**.

---

## 🧰 Stack I work in

<div align="center">

**Agentic AI & LLM systems**

`LangGraph` · `LangChain` · `Model Context Protocol` · `ReAct` · `Tool Calling` · `Multi-Agent Orchestration` · `RAG` · `FAISS` · `ChromaDB` · `pgvector` · `mem0` · `AWS Bedrock` · `Anthropic Claude` · `OpenAI GPT-4o` · `LLM Fine-Tuning`

**Evaluation, guardrails & reliability**

`Evaluation Harnesses` · `Golden Sets` · `Grounding Checks` · `Precision@K` · `MRR` · `Human-in-the-Loop Approval` · `PII Detection` · `Confidence Thresholds` · `Fallback Ladders` · `Dead-Letter Queues` · `Audit Trails`

**Languages**

[![Languages](https://skillicons.dev/icons?i=py,ts,java&perline=3)](https://skillicons.dev)

`Python` · `TypeScript` · `Java` · `SQL`

**Services & data**

[![Backend](https://skillicons.dev/icons?i=fastapi,spring,nodejs,postgres,redis,kafka&perline=6)](https://skillicons.dev)

**Cloud & delivery**

[![Cloud](https://skillicons.dev/icons?i=aws,docker,kubernetes,terraform,githubactions&perline=5)](https://skillicons.dev)

**Product surface**

[![Frontend](https://skillicons.dev/icons?i=react,nextjs,redux,tailwind&perline=4)](https://skillicons.dev)

</div>

<details>
<summary><b>Also used in shipped work, just not what I lead with</b></summary>

<br/>

`C++17` and `WebAssembly` (QuarkCache, AWL rendering engine) · `Go` (KubeGuard exporter, AWL WebSockets) · `C#` · `Azure` Event Hubs, Stream Analytics, Synapse (eduMorph) · `GCP` and `BigQuery ML` (RetailForecastAI) · `Databricks`, `Delta Lake`, `PySpark`, `Snowflake` (merger-lakehouse, Biodesign) · `Solidity` (veridiumMesh) · `RabbitMQ`, `Elasticsearch`, `MongoDB` · `Prometheus`, `Grafana` · `Streamlit`, `Power BI`, `Tableau`

</details>

---

## 🗂️ The engineering underneath

Agents fail like distributed systems. These are where I learned to handle that.

| Project | What it is | Stack |
|---|---|---|
| [Nexus](https://github.com/Brijesh03032001/Nexus) | Event-driven CRM — Kafka keeps AI enrichment off a sub-50 ms write path, Bedrock + FAISS lift dedupe 70%, RabbitMQ workers retry with a DLQ | Java · Spring Boot · Kafka · Bedrock |
| [quark-cache](https://github.com/Brijesh03032001/quark-cache) | Redis-like KV store from scratch — O(1) LRU, epoll/kqueue event loop, AOF with CRC32 and crash recovery | C++17 · FastAPI · Next.js |
| [merger-lakehouse](https://github.com/Brijesh03032001/merger-lakehouse) | Post-acquisition lakehouse — 20M rows in 584 s, SCD2 history, entity resolution at 99.4% precision resolving 91% without a human | Databricks · Delta Lake · PySpark |
| [KubeGuard](https://github.com/Brijesh03032001/KubeGuard) | AIOps agent predicting pod memory anomalies *before* the limit breaks, feeding the HPA, asking Gemini for one kubectl fix | Kubernetes · LSTM · LightGBM · Go |
| [RetailForecastAI](https://github.com/Brijesh03032001/RetailForecastAI) | Demand forecasting across 1,115 stores at 16.92% MAPE, with a RAG layer that explains each forecast | BigQuery ML · FastAPI · LangChain |
| [churnopt](https://github.com/Brijesh03032001/churnopt) | Churn prediction with dollar figures attached — leakage audit, calibration to 0.020 ECE, profit-backed contact policy | scikit-learn · DuckDB · Streamlit |
| [eduMorph](https://github.com/Brijesh03032001/eduMorph) | 1,000+ events/sec through Azure Event Hubs into Synapse, with 3 governed metric definitions | Azure · Stream Analytics · Power BI |
| [StudySliceAI](https://github.com/Brijesh03032001/StudySliceAI) | 3-hour lecture → 6–7 minutes of clips on autoscaled AWS. 🥈 Runner-up, SunHacks 2025 | AWS · Terraform · Gemini · FFmpeg |

<details>
<summary><b>📦 Six more — CV, blockchain, audio ML, SAP, analytics</b></summary>

<br/>

| Project | What it is | Stack |
|---|---|---|
| [StyleNova-AI](https://github.com/Brijesh03032001/StyleNova-AI) | CLIP visual embeddings blended with a per-user preference vector learned from swipes | PyTorch · CLIP · FastAPI |
| [veridiumMesh](https://github.com/Brijesh03032001/veridiumMesh) | AI-gated carbon credit issuance — risky credits blocked before mint, dual ECDSA, Merkle proofs | Solidity · Ethereum · scikit-learn |
| [EmotiSphere](https://github.com/Brijesh03032001/EmotiSphere) | Speech-intent platform for stuttered and accented speech, phoneme-accurate lip sync | React Three Fiber · Ollama |
| [EmotionClassifier](https://github.com/Brijesh03032001/EmotionClassifier) | Emotion-aware music retrieval — librosa DSP, clustering bake-off, pgvector search | librosa · Supabase · FastAPI |
| [SwiggyAnalysis](https://github.com/Brijesh03032001/SwiggyAnalysis) | 197,430 orders into a City Expansion Index and a Restaurant Health Score | Python · SciPy · Streamlit |
| [EnterpraNex](https://github.com/Brijesh03032001/EnterpraNex) | Enterprise workflow approval hub deployed to SAP BTP as an MTA | SAP CAP · UI5 · HANA Cloud |

</details>

Every repo has an architecture diagram, the engineering decisions behind it, and measured results — not just a stack list.

---

## 🏆 Achievements

|  |  |
|---|---|
| 📄 | **Sole-author Springer publication** — *Early Dementia Detection and Classification of Stage by Efficient Segmentation and Artificial Neural Network*, Smart Generation Computing and Communication Networks, 2026. **94%** accuracy on Alzheimer's-versus-Parkinson's FDG-PET classification — **[LINK](https://link.springer.com/chapter/10.1007/978-3-032-06798-2_8)** |
| 🎤 | Presented that paper at **Adv. Immunology 2026** in Amsterdam, October 21–22 |
| 🚀 | Accepted into **Y Combinator Startup School 2026** |
| 🌍 | Merged pull requests into **3 major open-source projects**, including Python repositories — **Open Source Super Contributor**, Hacktoberfest 2025 |
| 🥇 | **Top 0.2% in CodeKaze** — rank 315 of 150,000 · **1,000+ LeetCode problems** solved in C++ |
| 🎓 | Data Science Professional Certificate (IBM) · Deep Learning Specialization (DeepLearning.AI) |

**Hackathons**

| Result | Event | Project |
|---|---|---|
| 🥇 Winner | Kiro Spark Challenge 2026 — ASU × AWS, 24-hour build | [Ghosty](https://github.com/Brijesh03032001/Ghosty_A_Conference_helper) |
| 🥇 Winner | CrozeAI Hackathon | — |
| 🥈 Runner-up | SunHacks 2025, Education Track | [StudySliceAI](https://github.com/Brijesh03032001/StudySliceAI) |
| 🥉 Top 3 | EmotiSphere Hackathon | [SpeakSmart AI](https://github.com/Brijesh03032001/EmotiSphere) |
| 🎯 Finalist | JPMorgan Code for Good 2024 | — |

---

## 📊 GitHub at a glance

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Brijesh03032001&show_icons=true&hide=stars,issues&hide_rank=true&hide_border=true&theme=transparent&title_color=0969DA&icon_color=3178C6&text_color=7D8590)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Brijesh03032001&layout=compact&hide_border=true&theme=transparent&title_color=0969DA&text_color=7D8590&langs_count=8&hide=jupyter%20notebook,html,css,scss,hcl,tsql,php)

![GitHub Streak](https://streak-stats.demolab.com?user=Brijesh03032001&hide_border=true&theme=transparent&ring=0969DA&fire=C44F00&currStreakLabel=0969DA)

</div>

---

## 🤝 Let's build something

I want to work on agents that are trusted with real actions — the ones where a wrong call costs something, and someone has to be able to check it afterwards. That's why everything I ship has an evaluation harness, an approval gate or an audit trail beside it, and why I care as much about what happens when the model is wrong as when it's right.

If that's the problem you're hiring for, I'd love to talk.

<div align="center">

**[brijeshbuilds.com](https://brijeshbuilds.com) · [LinkedIn](https://linkedin.com/in/brijeshkumar03) · [kumarbrijesh.dev@gmail.com](mailto:kumarbrijesh.dev@gmail.com)**

</div>
