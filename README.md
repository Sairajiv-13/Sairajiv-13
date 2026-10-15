# Sai Rajiv Nagula

**Senior Generative AI Engineer | LLM, RAG & Agentic AI Systems**
Chicago, IL · Open to Senior AI Engineer roles across the US (remote first)

I build production GenAI systems, not demos. Eight years across data science, machine learning, and data engineering, currently Senior Generative AI Engineer at Mayo Clinic, previously Data Scientist at Google (via Wipro). My work is RAG and agentic systems that run under real constraints: HIPAA compliance, measured evaluation, cost control, and answers that can be traced back to a source.

Selected results from my recent work:

- Reduced LLM inference cost by 35% at Mayo Clinic by routing models on SageMaker with GPU auto-scaling
- Accelerated LLM training workflows by 40% with distributed training on SageMaker and PySpark on EMR
- Built HIPAA-compliant RAG over clinical knowledge with hybrid retrieval, reranking, and citation checking to reduce hallucinations

## Flagship projects

| Project | What it does | Proof in the repo |
|---|---|---|
| [enterprise-ai-ops-agent](https://github.com/Sairajiv-13/enterprise-ai-ops-agent) | LangGraph state machine that turns emails, tickets, Slack messages, and PDFs into finished work: classification, extraction, Jira tickets, drafted replies, and manager reports. FastAPI, Redis queue, JWT auth. | 159 tests, 86% coverage, mypy strict, eval harness, ADRs, Docker, runs with no external accounts |
| [rag-knowledge-platform](https://github.com/Sairajiv-13/rag-knowledge-platform) | Multi-tenant RAG service with hybrid retrieval (pgvector + full-text), grounded answers with verified citations, per-tenant isolation and quotas, and a live API. | 90 tests, 81% coverage, labeled retrieval eval set, benchmarks, Terraform, Terraform and an architecture diagram in the repo |
| [campaign-studio](https://github.com/Sairajiv-13/campaign-studio) | Generates email and SMS campaign variants per segment, then scores and ranks them on brand voice, clarity, CTA, and deliverability, measured against human judgment instead of model self-grading. | 77 tests, 94% coverage, 18-pair scoring validation, cost accounting, guardrails |

Each README states plainly what is tested, what is built but unproven at scale, and what the numbers actually come from. That is deliberate.

## Also here

- [hipaa-patient-portal](https://github.com/Sairajiv-13/hipaa-patient-portal): Terraform AWS infrastructure mapped to HIPAA technical safeguards, with encrypted RDS, VPC isolation, KMS, and CloudTrail audit logging

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
