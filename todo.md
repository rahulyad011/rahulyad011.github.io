# Portfolio Projects — Dev Backlog

Projects to build, finish, and add to index.html under the Projects section.
Each entry includes the planned stack, bullet descriptions (from the portfolio draft), and a checklist of tasks needed before it goes live.

---

## Project A — Autonomous Research Agent

**Stack:** OpenAI Agents SDK · GPT-4o · Tavily Search · Arxiv API · Qdrant · FastAPI · Streamlit · Python

**What it does:**
- Autonomous research agent that decomposes a research question, searches Arxiv and the web, retrieves and synthesizes findings, and produces a cited research report
- Implements a planner–executor–critic loop: planner decomposes, executor retrieves and summarizes, critic re-runs on identified gaps until coverage threshold is met
- Output: PDF report with citations, per-claim confidence scores, and follow-up question set; deployed with FastAPI + Streamlit

**Tasks:**
- [ ] Build planner–executor–critic loop
- [ ] Integrate Tavily Search + Arxiv API tools
- [ ] Set up Qdrant vector store for retrieved chunks
- [ ] Implement PDF report generator with citations and confidence scores
- [ ] Wrap in FastAPI backend + Streamlit UI
- [ ] Push code to GitHub (`autonomous-research-agent` repo)
- [ ] Record or screenshot a demo
- [ ] Add to index.html under "Intelligent Agents & RAG Systems"

---

## Project B — Multi-Agent Code Review System

**Stack:** OpenAI Agents SDK · GPT-4o · GitHub Webhooks · AST parsing · Pydantic v2 · FastAPI · Python

**What it does:**
- Multi-agent system where specialists review for security, performance, style, test coverage, and documentation in parallel; meta-agent synthesizes a structured PR review
- Integrates with GitHub PRs via webhook; each agent emits Pydantic-validated structured output for deterministic downstream processing
- Produces severity-ranked findings, suggested fixes, and a pass/fail recommendation — reduces manual code review time on routine PRs

**Tasks:**
- [ ] Define specialist agents (security, performance, style, test coverage, docs)
- [ ] Build meta-agent that synthesizes all agent outputs
- [ ] Set up GitHub webhook integration
- [ ] Implement Pydantic v2 structured output schemas per agent
- [ ] Build severity-ranking and pass/fail logic
- [ ] Push code to GitHub (`multi-agent-code-review` repo)
- [ ] Add to index.html under "Code Intelligence & Developer Tooling"

---

## Project C — Agentic Data Pipeline Debugger

**Stack:** OpenAI Agents SDK · GPT-4o · Apache Airflow API · Great Expectations · Grafana API · Python

**What it does:**
- AI agent that monitors ML data pipelines, autonomously diagnoses failures (schema drift, null spikes, distribution shift), traces root causes across stages, and proposes remediation
- Tool-calling agent queries Airflow logs, runs statistical tests, cross-references upstream sources, and classifies failure type
- Reduces mean-time-to-pipeline-recovery (MTTPR) by automating triage that typically takes a data engineer hours of manual digging

**Tasks:**
- [ ] Wire up Airflow API as agent tool (log fetching, DAG status)
- [ ] Integrate Great Expectations for schema/quality checks
- [ ] Integrate Grafana API for metric queries
- [ ] Build failure classifier (schema drift, null spike, distribution shift)
- [ ] Implement root-cause trace + remediation recommendation output
- [ ] Push code to GitHub (`agentic-pipeline-debugger` repo)
- [ ] Add to index.html under "Analytics & Monitoring"

---

## Project D — LLM Evaluation & Benchmarking Harness

**Stack:** OpenAI Agents SDK · GPT-4o · Claude · Phoenix Tracing · Pydantic Evals · LangSmith · Streamlit · Python

**What it does:**
- Evaluation harness that runs side-by-side benchmarks across multiple LLM providers (OpenAI, Anthropic, open-source) on custom task suites
- Implements LLM-as-judge with calibration against human gold labels, plus deterministic metrics (BLEU, ROUGE, exact match, semantic similarity)
- Produces a leaderboard dashboard with cost-per-task, latency distribution, and quality score

**Tasks:**
- [ ] Build provider-agnostic LLM runner (OpenAI, Anthropic, open-source)
- [ ] Implement LLM-as-judge with calibration against human labels
- [ ] Add deterministic metrics (BLEU, ROUGE, exact match, semantic similarity)
- [ ] Wire up Phoenix Tracing + LangSmith for observability
- [ ] Build Streamlit leaderboard dashboard (cost, latency, quality)
- [ ] Push code to GitHub (`llm-eval-harness` repo)
- [ ] Add to index.html under "Intelligent Agents & RAG Systems"

---

## Project E — Real-Time Multimodal Sentiment & Trend Monitor

**Stack:** OpenAI Agents SDK · GPT-4o · Whisper · Reddit API · Apache Kafka · ClickHouse · Grafana · Python

**What it does:**
- Streaming multi-agent pipeline ingesting text (social), audio (podcasts/earnings), and structured feeds in real time via Kafka
- Per-modality agents: sentiment classifier, trend detector (sliding-window), alert agent that fires on signal convergence or anomalies
- Live Grafana dashboard with per-entity trend, cross-modal convergence, and auto-generated narrative summary of the current market story

**Tasks:**
- [ ] Set up Kafka streaming pipeline for text + audio + structured feeds
- [ ] Build per-modality agents (sentiment, trend, alert)
- [ ] Integrate Reddit API for social ingestion
- [ ] Integrate Whisper for audio transcription
- [ ] Set up ClickHouse for time-series storage
- [ ] Build Grafana dashboard (per-entity trend, convergence, narrative)
- [ ] Push code to GitHub (`multimodal-sentiment-monitor` repo)
- [ ] Add to index.html under "Analytics & Monitoring"

---

## Project F — Agentic ML Experiment Orchestrator

**Stack:** OpenAI Agents SDK · GPT-4o · MLflow · Optuna · scikit-learn · PyTorch · FastAPI · Python

**What it does:**
- Autonomous AI agent that designs, runs, evaluates, and iterates ML experiments — given a dataset and goal metric, selects architectures, configures HPO search spaces, monitors results, proposes next experiments
- Implements a hypothesis-driven loop: agent generates hypothesis → runs experiment → evaluates → updates belief state → next hypothesis
- Reduces time-to-best-model on tabular/NLP tasks by replacing manual experiment design with autonomous LLM-guided search

**Tasks:**
- [ ] Build hypothesis-driven experiment loop
- [ ] Integrate MLflow for experiment tracking
- [ ] Integrate Optuna for HPO search space configuration
- [ ] Support tabular (scikit-learn / XGBoost) and NLP (PyTorch) experiment types
- [ ] Build belief-state tracker across experiment iterations
- [ ] Wrap in FastAPI for programmatic access
- [ ] Push code to GitHub (`agentic-ml-orchestrator` repo)
- [ ] Add to index.html under "Intelligent Agents & RAG Systems"

---

## Project G — Voice-First AI Assistant for Domain Experts

**Stack:** OpenAI Realtime API · Whisper · TTS · OpenAI Agents SDK · Twilio · FastAPI · Python

**What it does:**
- Voice-first conversational AI assistant designed for non-technical domain experts (e.g., field inspectors, healthcare workers, legal professionals)
- Real-time speech in/out via OpenAI Realtime API; tool-calling agent backbone for retrieving from domain knowledge bases and structured systems
- Demonstrates the next frontier of AI UX — natural voice + agent reasoning + structured tool calls — applicable across industries

**Tasks:**
- [ ] Set up OpenAI Realtime API for speech-in / speech-out
- [ ] Build tool-calling agent backbone (domain KB retrieval + structured system queries)
- [ ] Integrate Twilio for phone/voice channel (optional)
- [ ] Build a demo domain (e.g., field inspector assistant with a sample knowledge base)
- [ ] Deploy with FastAPI
- [ ] Record a demo video
- [ ] Push code to GitHub (`voice-first-ai-assistant` repo)
- [ ] Add to index.html under "Intelligent Agents & RAG Systems"

---

## How to re-add a project to index.html

1. Build the project and push code to GitHub
2. Copy the relevant `<tr>` block template from a similar existing project in index.html
3. Update: title, stack line, bullet descriptions, GitHub link, demo link (if any), image
4. Place under the appropriate section header (see groupings in index.html)
5. Remove the project from this file once it's live
