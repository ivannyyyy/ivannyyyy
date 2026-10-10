<p align="center">
  <img src="./assets/profile-banner.gif" width="100%" alt="Ivan Borovskikh — AI Automation Engineer" />
</p>

<div align="center">

# Ivan Borovskikh

### AI Automation Engineer

**LLM Applications · AI Agents · Integrations · Workflow Automation**

`business process → working end-to-end system`

</div>

---

## About

I build applied AI automation systems: agent workflows, LLM-powered processes, API integrations, persistent context and human-in-the-loop scenarios.

My focus is not just generating model responses, but turning a real business process into a reliable system with clear states, deterministic rules, model-driven decisions and end-to-end execution.

## What I build

- **AI agents & LLM workflows** — roles, goals, rules, context, structured output and state routing
- **Workflow automation** — scheduled and event-driven pipelines, retries and error handling
- **Integrations** — REST API, HTTP, JSON, webhooks, Telegram and external services
- **Data & state** — PostgreSQL, Supabase, Airtable, conversation history and document flows
- **Human-in-the-loop systems** — escalation to an administrator when the model does not have enough information
- **AI content systems** — generation, quality control, asset processing and automated publishing

## Featured Projects

### [AI Content Pipeline for n8n](https://github.com/ivannyyyy/ai-content-pipeline-n8n)

<p align="center">
  <img src="./assets/content-pipeline-pixel.png" width="100%" alt="AI Content Pipeline — generation, quality control and publishing workflow" />
</p>

An AI-powered content production pipeline split into independent workflows:

```text
Source data
    ↓
AI generation & rewriting
    ↓
Media generation
    ↓
AI quality control
    ↓
Scheduling
    ↓
Telegram / MAX
```

The production version was built for channels with a combined audience of **1M+** and automated the main content-production stages, reducing manual operations by **80–90%**.

---

### [Human-in-the-Loop Telegram AI Assistant](https://github.com/ivannyyyy/telegram-ai-assistant-n8n)

<p align="center">
  <img src="./assets/telegram-ai-assistant-pixel.png" width="100%" alt="Telegram AI Assistant — durable events, stateful dialogue and human escalation" />
</p>

A task-driven Telegram AI assistant with **two preserved architecture iterations**. The repository shows the evolution from a workflow-centric v1 to a v2 runtime built around durable PostgreSQL events, explicit messages/facts/owner requests, deterministic Agent Core routing and asynchronous human escalation.

```text
v1
workflow orchestration around an LLM
        ↓
known runtime limitations
        ↓
architecture redesign
        ↓
v2
durable event queue
+ explicit runtime state
+ async human-in-the-loop
+ reconciliation & completion workers
```

The public project contains **18 sanitized n8n workflows**: 11 from v1 and 7 from the completed v2 redesign.

**v2 highlights:** `FOR UPDATE SKIP LOCKED` event claiming · task/dialog state separation · confirmed facts with scoped reuse · non-blocking owner requests · Telegram routing guards · durable completion notifications · PostgreSQL file cache

**Core stack:** n8n · Airtable · PostgreSQL · OpenAI · Telegram / TelePilot · Cloudinary (v1)

---

### [Retrieval & RAG Patterns with n8n](https://github.com/ivannyyyy/n8n-retrieval-rag-patterns)

A compact retrieval-focused project showing when to use deterministic SQL lookup and when to use a full RAG pipeline for unstructured documents.

```text
Structured data → PostgreSQL tool → deterministic lookup

Unstructured docs
        ↓
chunking + embeddings
        ↓
PGVector + PostgreSQL FTS
        ↓
merge + deduplicate
        ↓
Cohere rerank
        ↓
grounded answer with sources
```

**Highlights:** RAG · PGVector · OpenAI embeddings · hybrid retrieval · PostgreSQL full-text search · Cohere reranking · document ingestion · source attribution

## Technologies

| Area | Tools & technologies |
|---|---|
| **AI & LLM** | OpenAI API, Gemini API, AI agents, RAG, embeddings, hybrid retrieval, reranking, prompt engineering, structured output, context engineering |
| **Automation** | n8n, workflow orchestration, scheduling, event and error handling |
| **Backend & data** | Python — basic level & scripts, SQL — basic queries, PostgreSQL, PGVector, Supabase, Airtable |
| **Integrations** | REST API, HTTP, JSON, webhooks, Telegram integrations, Cloudinary, Google Drive |
| **Agent tooling** | MCP tools and integrations |
| **Generative workflows** | AI image & video pipelines |

## How I approach automation

```text
UNDERSTAND → STRUCTURE → AUTOMATE → OBSERVE → IMPROVE
```

I separate deterministic business rules from model decisions, keep state and history explicit, and design automation so that uncertain cases can be handed back to a human instead of being invented by the model.

---

<div align="center">

**Build systems that remove routine work — not human judgment.**

</div>
