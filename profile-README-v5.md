# Sai Rajiv Nagula

Senior Generative AI Engineer at Mayo Clinic, Chicago.

I build LLM systems that run in production: retrieval, agents, and the evaluation work that keeps both honest. Eight years across machine learning, data science, and data engineering. At Mayo Clinic my work is RAG over clinical knowledge and agentic workflows on AWS Bedrock and SageMaker, built under HIPAA constraints: measured evaluation, cost control, and answers that trace back to a source.

Day to day: Python, FastAPI, LangGraph, PostgreSQL with pgvector, AWS Bedrock and SageMaker, Docker.

## Projects

The five main projects. Each is held to the same bar: green CI, a tagged release, measured results, and proof a reviewer can click.

- [rag-knowledge-platform](https://github.com/Sairajiv-13/rag-knowledge-platform): multi-tenant RAG service with hybrid retrieval, verified citations, and per-tenant quotas. Measured retrieval eval and benchmarks in the repo. [Live demo](https://rag-knowledge-platform-rnsc.onrender.com/docs), container image on GHCR.
- [enterprise-ai-ops-agent](https://github.com/Sairajiv-13/enterprise-ai-ops-agent): a LangGraph state machine that turns email, tickets, chat messages, and PDFs into finished work: tickets opened, replies drafted, reports written. 159 tests, an eval harness, and an ADR for every real decision.
- [pr-review-agent](https://github.com/Sairajiv-13/pr-review-agent): an AI pull request reviewer as a CLI and a GitHub Action. Its own review is posted on [the demo pull request](https://github.com/Sairajiv-13/pr-review-agent/pull/1).
- [clinical-trials-mcp-server](https://github.com/Sairajiv-13/clinical-trials-mcp-server): an MCP server over the ClinicalTrials.gov API. Eligibility is decided only where the criteria are deterministic; the rest is returned for the caller to judge.
- [campaign-studio](https://github.com/Sairajiv-13/campaign-studio): generates campaign variants per segment and scores them against human judgment instead of model self-grading. Ranking accuracy is a CI gate.

Applied ML and data projects, each live:

- [hospital-readmission-api](https://github.com/Sairajiv-13/hospital-readmission-api): readmission risk API on the UCI Diabetes dataset, patient-grouped split, tuned decision threshold, drift checks. [Live](https://hospital-readmission-api-ec05.onrender.com/docs)
- [telco-churn-analysis](https://github.com/Sairajiv-13/telco-churn-analysis): churn analysis on the IBM Telco data with executed notebooks, a findings document, and a scoring app. [Live](https://telco-churn-analysis-t5rx.onrender.com)
- [recommendation-engine](https://github.com/Sairajiv-13/recommendation-engine): three recommenders compared on the same MovieLens holdout, served with a cold-start path. [Live](https://recommendation-engine-a8e4.onrender.com)

## Selected design docs

The decisions behind these projects, written as ADRs with the rejected alternatives named:

- [Tenant isolation](https://github.com/Sairajiv-13/rag-knowledge-platform/blob/main/docs/adr/0002-tenant-isolation.md): keeping one tenant's data out of another's answers
- [Hybrid retrieval](https://github.com/Sairajiv-13/rag-knowledge-platform/blob/main/docs/adr/0003-hybrid-retrieval.md): why dense and keyword search run together, with the measurements
- [Evaluation and quality gates](https://github.com/Sairajiv-13/enterprise-ai-ops-agent/blob/main/docs/adr/0009-evaluation-and-quality-gates.md): how non-deterministic output gets measured before it ships
- [Idempotency strategy](https://github.com/Sairajiv-13/enterprise-ai-ops-agent/blob/main/docs/adr/0017-idempotency-strategy.md): making retries safe in a pipeline that takes real actions

## Open source

- LangChain: root-caused a dropped evaluation config in the tracer callback chain, [issue #31802](https://github.com/langchain-ai/langchain/issues/31802), fix and regression tests in [PR #41251](https://github.com/langchain-ai/langchain/pull/41251)
- FastMCP: verified the error-handling behavior from the client side and proposed the documentation fix on [issue #5564](https://github.com/PrefectHQ/fastmcp/issues/5564)

## How I build

- Evaluation before claims: labeled eval sets, reproducible benchmarks, no invented metrics
- Architecture decisions written down as ADRs, with the rejected alternatives named
- Tests, typing, and CI as part of the project, not an afterthought
- Limitations stated in every README, next to the claims they limit

## Background

- Senior Generative AI Engineer, Mayo Clinic (2024 to present)
- M.S. Information Systems, DePaul University (2025)
- B.Tech Computer Science, Kakatiya University (2018)

## Connect

- LinkedIn: https://www.linkedin.com/in/rajivn3/
- Email: sairn3@gmail.com
