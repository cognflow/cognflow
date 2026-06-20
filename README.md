

# 👋 Hi, I'm Ogaji Igwe Samuel

### AI Automation Engineer • n8n Builder • DevOps & Cloud Engineer
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/0f7a190b-5fcf-433f-a4b4-52d74aae10e7" />

# Cognflow

AI business automation engineering. We design and ship production-grade automation systems — not demos — using agentic AI, workflow orchestration platforms, and cloud-native infrastructure.

Built and maintained by [Ogaji igwe samuel](https://github.com/cognflow).

## Philosophy

Automation is only valuable when it removes real operational friction. Every system here is built with production-style data, real API integrations, and documented engineering decisions — including the debugging, not just the demo.

We build three things:

1. **Workflow automations** in n8n and Make.com — fast to build, easy to hand off, ideal for teams that need automation without a custom backend.
2. **Standalone backend services** in Python — for cases where a no-code platform's limits matter: custom agentic logic, full infrastructure ownership, or production-grade reliability requirements.
3. **Cloud infrastructure** — every backend service is deployed with Terraform-managed AWS infrastructure and CI/CD, not manually configured.

## Repositories

### [n8n-automation-templates](https://github.com/cognflow/n8n-automation-templates)
10 production-style n8n workflows covering lead capture, client onboarding, support triage, proposal generation, RAG knowledge retrieval, and a fully autonomous AI sales agent.

| Workflow | What it does |
|---|---|
| P01 — AI Lead Capture & Response | Qualifies inbound leads with Claude, sends a personalized response automatically |
| P03 — AI Client Onboarding Engine | Triggers a multi-step onboarding sequence when a client goes active in Notion |
| P05 — AI Customer Support Triage | Classifies tickets by urgency and category, routes via conditional logic |
| P08 — AI Proposal Generator | Turns a client brief into a full proposal document, generated and delivered automatically |
| P09 — RAG Business Knowledge Bot | In-memory RAG system — Cohere embeddings, cosine similarity, no vector database — grounded in a Notion knowledge base |
| P10 — Autonomous AI Sales Agent | End-to-end: qualifies leads, scores intent, creates CRM records, retrieves SOP context, generates and sends outreach, updates audit trails, fires Slack alerts. No human intervention required. |

**Stack:** n8n, Claude, Notion API, Gmail API, Slack API, Cohere, Google Docs API, Docker.

### [make-automation-templates](https://github.com/cognflow/make-automation-templates)
A second automation portfolio built on Make.com, demonstrating the same patterns on a different orchestration platform.

| Module | What it does |
|---|---|
| M01 — AI Lead Scoring & CRM Sync | Tally form submissions scored by Claude, synced to an Airtable CRM |
| M02 — Social Media Content Engine | Generates platform-specific captions (LinkedIn, Instagram, X) from content briefs |
| M03 — AI Invoice & Payment Tracker | Extracts invoice data from Gmail, logs to Notion and Google Sheets, sends automated payment reminders |
| M04 — Customer Support Auto-Responder | Classifies and responds to support tickets automatically — also rebuilt standalone, see AutoFlow API below |

**Stack:** Make.com, Claude, Airtable, Google Sheets, Notion, Gmail.

### [autoflow-api](https://github.com/cognflow/autoflow-api)
A standalone, production-grade rebuild of the M04 support automation — built in Python with Claude's agentic tool use, fully infrastructure-as-code on AWS, deployed via CI/CD.

A support ticket comes in via webhook → Claude classifies it and decides which tools to call → logs the ticket to Notion → drafts and sends a reply via Amazon SES. No hardcoded branching — the model owns the decision sequence at runtime.

**Stack:** FastAPI, Anthropic SDK, PostgreSQL (RDS), Notion API, Amazon SES, ECS Fargate, Terraform, GitHub Actions with OIDC.

This repo exists to demonstrate the difference between orchestrating an automation on a no-code platform and owning the full stack: application code, AI orchestration logic, network architecture, IAM boundaries, and CI/CD — including the real debugging that production infrastructure surfaces and a no-code platform abstracts away.

## Engineering patterns across all three

- **Agentic AI decision-making** — Claude decides which tools to call and in what order, rather than following a fixed branch structure
- **Structured JSON outputs** from Claude, parsed and routed programmatically
- **RAG without managed infrastructure** — in-memory vector search where a full vector database would be overkill
- **Production-style testing** — every workflow and service tested against realistic data and signed/authenticated requests, not toy inputs
- **Infrastructure as code** — the AutoFlow API's AWS footprint is fully reproducible and disposable via Terraform
- **CI/CD without long-lived credentials** — GitHub Actions assumes scoped AWS roles via OIDC, not static access keys

## Tech stack, org-wide

| Category | Tools |
|---|---|
| Orchestration | n8n, Make.com |
| AI | Anthropic Claude (agentic tool use), Cohere (embeddings) |
| Backend | FastAPI, Python, PostgreSQL |
| Cloud | AWS (ECS Fargate, RDS, SES, Secrets Manager, VPC), Terraform |
| CI/CD | GitHub Actions, OIDC federation |
| Integrations | Notion, Airtable, Gmail, Slack, Google Sheets/Docs |
| Containerization | Docker |

## Quick start — n8n workflows

```bash
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  -v n8n_data:/home/node/.n8n \
  n8nio/n8n
```

Then import any workflow JSON from `n8n-automation-templates/workflows/` and configure credentials.

## Connect

- GitHub: [github.com/cognflow](https://github.com/cognflow)
- LinkedIn: [linkedin.com/in/igwe-ogaji](https://linkedin.com/in/igwe-ogaji)
- Email: samklinofficial91@gmail.com

## License

MIT — free to use, modify, and distribute.
