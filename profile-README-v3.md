# Sai Rajiv Nagula

**Senior Generative AI Engineer | LLM, RAG & Agentic AI Systems | Mayo Clinic, previously at Google**
Chicago, IL · Open to Senior AI Engineer roles across the US (remote first)

I build production GenAI systems, not demos. Eight years across data science, machine learning, and data engineering, currently Senior Generative AI Engineer at Mayo Clinic, previously Data Scientist at Google (via Wipro). My work is RAG and agentic systems that run under real constraints: HIPAA compliance, measured evaluation, cost control, and answers that can be traced back to a source.

Selected results from my recent work:

- Reduced LLM inference cost by 35% at Mayo Clinic by routing models on SageMaker with GPU auto-scaling
- Accelerated LLM training workflows by 40% with distributed training on SageMaker and PySpark on EMR
- Built HIPAA-compliant RAG over clinical knowledge with hybrid retrieval, reranking, and citation checking to reduce hallucinations
- At Google (via Wipro, 2021 to 2023): built RAG and semantic search systems, fine-tuned BERT models, and ran ML pipelines on Vertex AI with MLflow tracking and BigQuery and Dataflow pipelines at multi-terabyte scale

## Flagship projects

| Project | What it does | Proof in the repo |
|---|---|---|
| [rag-knowledge-platform](https://github.com/Sairajiv-13/rag-knowledge-platform) | Multi-tenant RAG service with hybrid retrieval (pgvector + full-text), grounded answers with verified citations, per-tenant isolation and quotas, and a documented API. | 90 tests, 81% coverage, measured hybrid retrieval eval (hit@1 0.553 vs 0.474 dense), benchmarks, container image on GHCR |
| [enterprise-ai-ops-agent](https://github.com/Sairajiv-13/enterprise-ai-ops-agent) | LangGraph state machine that turns emails, tickets, Slack messages, and PDFs into finished work: classification, extraction, Jira tickets, drafted replies, and manager reports. FastAPI, Redis queue, JWT auth. | 159 tests, 86% coverage, mypy strict, eval harness, ADRs, Docker, runs with no external accounts |
| [campaign-studio](https://github.com/Sairajiv-13/campaign-studio) | Generates email and SMS campaign variants per segment, then scores and ranks them on brand voice, clarity, CTA, and deliverability, measured against human judgment instead of model self-grading. | 77 tests, 94% coverage, 18-pair scoring validation, cost accounting, guardrails |
| [pr-review-agent](https://github.com/Sairajiv-13/pr-review-agent) | AI pull request reviewer that runs as a CLI and a GitHub Action. Findings land on exact diff lines, secret checks never print matched values, and dry run is the default. | 36 tests, 89% coverage, and the action's own review posted on [its demo PR](https://github.com/Sairajiv-13/pr-review-agent/pull/1) |
| [clinical-trials-mcp-server](https://github.com/Sairajiv-13/clinical-trials-mcp-server) | MCP server over the public ClinicalTrials.gov API: trial search, eligibility checks, and recruiting sites for any MCP client. | 73 tests, 92% coverage, container image on GHCR, eligibility decided only where it is deterministic |

## Applied ML and data projects

Production ML and data work: a clinical risk API, a churn analysis with a scoring app, and a recommendation engine. Each one tested, released, and running live.

| Project | What it does | Live |
|---|---|---|
| [hospital-readmission-api](https://github.com/Sairajiv-13/hospital-readmission-api) | Readmission risk API: three models compared on the UCI Diabetes dataset with a patient-grouped split, a tuned decision threshold, and PSI drift checks, served by FastAPI. | [Live API](https://hospital-readmission-api-ec05.onrender.com/docs) |
| [telco-churn-analysis](https://github.com/Sairajiv-13/telco-churn-analysis) | Churn analysis on the IBM Telco data: executed notebooks, a findings document with segment economics, and an app that scores a customer profile. | [Live app](https://telco-churn-analysis-t5rx.onrender.com) |
| [recommendation-engine](https://github.com/Sairajiv-13/recommendation-engine) | Movie recommendations on MovieLens: popularity, item-item cosine, and SVD compared on the same holdout, served by FastAPI with a cold-start path. | [Live demo](https://recommendation-engine-a8e4.onrender.com) |

Each README states plainly what is tested, what is built but unproven at scale, and what the numbers actually come from. That is deliberate.

## Selected design docs

The decisions behind the projects above, written as ADRs with the rejected alternatives named. These are the documents I would bring to a design review:

- [LangGraph orchestration](https://github.com/Sairajiv-13/enterprise-ai-ops-agent/blob/main/docs/adr/0003-langgraph-orchestration.md): why the pipeline is an explicit state machine, not a free-form agent loop
- [Evaluation and quality gates](https://github.com/Sairajiv-13/enterprise-ai-ops-agent/blob/main/docs/adr/0009-evaluation-and-quality-gates.md): how non-deterministic output gets measured before it ships
- [Idempotency strategy](https://github.com/Sairajiv-13/enterprise-ai-ops-agent/blob/main/docs/adr/0017-idempotency-strategy.md): making retries safe in a pipeline that takes real actions
- [Tenant isolation](https://github.com/Sairajiv-13/rag-knowledge-platform/blob/main/docs/adr/0002-tenant-isolation.md): keeping one tenant's data out of another's answers
- [Hybrid retrieval](https://github.com/Sairajiv-13/rag-knowledge-platform/blob/main/docs/adr/0003-hybrid-retrieval.md): why pgvector dense search and Postgres full-text run together, with a per-source score breakdown
- [Prompt injection and output escaping](https://github.com/Sairajiv-13/campaign-studio/blob/main/docs/adr/010-prompt-injection-and-output-escaping.md): the guardrails around generated copy

## Open source

- LangChain: root-caused a dropped evaluation config in the tracer callback chain, [issue #31802](https://github.com/langchain-ai/langchain/issues/31802), fix and regression tests in [PR #41251](https://github.com/langchain-ai/langchain/pull/41251)
- FastMCP: verified error-handling taxonomy from the client side and proposed the documentation fix on [issue #5564](https://github.com/PrefectHQ/fastmcp/issues/5564)

## Stack I work in

- **GenAI / LLM:** OpenAI, Azure OpenAI, Anthropic Claude, AWS Bedrock, LangChain, LangGraph, LlamaIndex, Hugging Face, RAG and advanced RAG, fine-tuning (LoRA, QLoRA, PEFT), MCP / FastMCP
- **ML / Data:** Python, PyTorch, TensorFlow, scikit-learn, Spark / PySpark, Kafka, Airflow, Snowflake, Databricks
- **Platform:** AWS (SageMaker, Bedrock, OpenSearch, Lambda, Textract), Azure, GCP Vertex AI, Docker, Kubernetes, Terraform, MLflow
- **APIs / Data stores:** FastAPI, PostgreSQL / pgvector, Redis, MongoDB, vector search and hybrid retrieval
- **Observability:** Prometheus, Grafana, model monitoring, drift and latency tracking

## How I build

- Evaluation before claims: labeled eval sets, reproducible benchmarks, no invented metrics
- Architecture decisions written down as ADRs, with the rejected alternatives named
- Tests, typing, and CI as part of the project, not an afterthought
- Honest limitations in every README

## Background

- Senior Generative AI Engineer, Mayo Clinic (2024 to present): Bedrock and SageMaker RAG, agentic workflows with Bedrock Agents and Step Functions, OCR and document intelligence, HIPAA-compliant PHI processing
- Data Scientist, GenAI / ML, Google via Wipro (2021 to 2023): RAG and semantic search, BERT fine-tuning, Vertex AI and MLflow MLOps, BigQuery and Dataflow pipelines at multi-terabyte scale
- M.S. Information Systems, DePaul University (2025)
- B.Tech Computer Science, Kakatiya University (2018)

## Connect

- LinkedIn: https://www.linkedin.com/in/rajivn3/
- Email: sairn3@gmail.com
- GitHub: https://github.com/Sairajiv-13
