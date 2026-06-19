

# 👋 Hi, I'm Ogaji Igwe Samuel

### AI Automation Engineer • n8n Builder • DevOps & Cloud Engineer
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/0f7a190b-5fcf-433f-a4b4-52d74aae10e7" />

I build production-ready AI automation systems using **n8n, Claude, Notion, Slack, Gmail, Cohere, and modern cloud tooling**.

My focus is simple:

> Eliminate repetitive business operations with intelligent workflows.

From AI-powered onboarding systems to fully autonomous sales pipelines, I design automations that behave like operational infrastructure — not demos.

---

# 🚀 Cognflow — n8n Automation Templates

Production-ready AI-powered workflows built with n8n.

### 10 workflows. 1 portfolio. Built from scratch.

This repository contains the complete **Cognflow AI Automation Portfolio** — a collection of real-world automation systems covering:

* AI lead generation
* Client onboarding
* Customer support triage
* Proposal generation
* RAG knowledge retrieval
* Autonomous AI sales operations
* Social media automation
* Invoice processing

Every workflow is:

* Fully documented
* Built with real APIs
* Tested with production-style data
* Ready to import into n8n

---

# 🧠 Tech Stack

| Tool             | Purpose                    |
| ---------------- | -------------------------- |
| n8n              | Workflow orchestration     |
| Anthropic Claude | AI reasoning + generation  |
| Notion API       | CRM + knowledge base       |
| Gmail API        | Automated outreach         |
| Slack API        | Alerts + notifications     |
| Cohere           | Text embeddings for RAG    |
| Google Docs API  | Proposal generation        |
| Docker           | Self-hosted infrastructure |

---

# 📦 Featured Workflows

## P01 — AI Lead Capture & Response

Receives inbound leads through a webhook, qualifies them with Claude, generates a personalised response email, and sends it automatically.

**Patterns used**

* Prompt engineering
* API orchestration
* Automated email workflows

---

## P03 — AI Client Onboarding Engine

Triggers automatically when a client becomes active in Notion and launches a multi-step onboarding process.

**Patterns used**

* Stateful workflow sequencing
* Cross-node data referencing
* Automated onboarding systems

---

## P05 — AI Customer Support Triage

Uses Claude to classify support tickets by urgency and category, then routes them automatically through conditional logic.

**Patterns used**

* Structured JSON prompting
* Switch node routing
* AI classification pipelines

---

## P08 — AI Proposal Generator

Transforms a client brief into a complete business proposal using Claude, generates a Google Doc, and emails it automatically.

**Patterns used**

* Long-form AI generation
* Dynamic document creation
* Automated delivery workflows

---

## P09 — RAG Business Knowledge Bot

A fully in-memory RAG system built entirely in n8n — no Pinecone, no LangChain, no vector database.

### Features

* Notion knowledge retrieval
* Cohere embeddings
* Cosine similarity search
* In-memory vector storage
* Claude grounded responses

**Patterns used**

* Batch embedding requests
* RAG retrieval pipelines
* Vector similarity search in JavaScript

---

## P10 — Autonomous AI Sales Agent

The flagship Cognflow system.

A complete autonomous sales workflow that:

* Qualifies leads
* Scores intent
* Creates CRM records
* Retrieves SOP context
* Generates outreach emails
* Sends emails automatically
* Updates audit trails
* Fires Slack alerts

No human intervention required.

### Key Engineering Patterns

* Agentic AI decision pipelines
* Structured Claude JSON outputs
* JSON.stringify() payload serialization
* RAG-assisted outreach generation
* Full CRM lifecycle automation

---

# 🛠 Repository Structure

```bash
cognflow/n8n-automation-templates/
├── README.md
└── workflows/
    ├── P01-AI-Lead-Capture-Response/
    ├── P03-AI-Client-Onboarding-Engine/
    ├── P05-AI-Customer-Support-Triage/
    ├── P08-AI-Proposal-Generator/
    ├── P09-RAG-Business-Knowledge-Bot/
    └── P10-Autonomous-AI-Sales-Agent/
```

# ⚡ Quick Start

## Run n8n via Docker

```bash
docker run -it --rm \
--name n8n \
-p 5678:5678 \
-v n8n_data:/home/node/.n8n \
n8nio/n8n
```

## Import a Workflow

1. Open n8n
2. Create New Workflow
3. Import from file
4. Configure credentials
5. Activate workflow

---

# 🔐 Integrations

### Anthropic Claude

* Header Auth
* `x-api-key`

### Notion API

* Internal integrations
* CRM + logging workflows

### Gmail / Slack

* OAuth2 integrations
* Notification automation

---

# 📚 Current Focus

* AI workflow orchestration
* Agentic automation systems
* RAG architectures in n8n
* DevOps + cloud infrastructure
* AI operations engineering

---

# 🌍 Connect With Me

* GitHub: github.com/cognflow
* LinkedIn: linkedin.com/in/igwe-ogaji
* Email: samuelaiautomation25@gmail.com

---

# 📌 Philosophy

> AI becomes valuable when it removes operational friction.

I don't build AI demos.

I build systems that:

* reduce manual work,
* improve operational speed,
* and scale business processes automatically.

---

# 📄 License

MIT — free to use, modify, and distribute.
