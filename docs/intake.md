# Intake Management 

## Overview

Every architecture practice needs a way to **intake, size, and prioritize** incoming work — whether it’s new product features, platform enhancements, technical debt, or compliance initiatives.

Effective intake management ensures that **architecture capacity is spent on the right things**, at the right time, with the right stakeholders engaged early.

This process should be **lightweight, transparent, and collaborative**, aligning closely with **product, engineering, and security** teams — not acting as a gatekeeper, but as an **enabler** of delivery flow and strategic alignment.

---

## Purpose

The purpose of intake and prioritization is to:

- **Provide clarity** on what architectural work is needed and why.  
- **Balance demand and capacity** across the solution and architecture teams.  
- **Enable early engagement** between architecture, product, engineering, and security.  
- **Surface cross-cutting concerns** (e.g., integration, NFRs, security, compliance) early.  
- **Align investment and sequencing** with enterprise and product priorities.

---

## Guiding Principles

1. **Lean over bureaucratic:** Keep intake friction low; use simple forms or Kanban cards, not Word templates.  
2. **Visible over hidden:** Make the pipeline of architectural work transparent to all stakeholders.  
3. **Collaborative over unilateral:** Prioritize jointly with product, engineering, and security.  
4. **Outcome-driven:** Focus on value and impact, not volume of requests.  
5. **Continuous, not episodic:** Intake happens continuously, not once per quarter.

---

## Core Roles and Responsibilities

| Role | Key Contributions |
|------|--------------------|
| **Product Management** | Defines business outcomes, product vision, and priorities. Identifies new initiatives requiring architecture support. |
| **Engineering / Delivery Leads** | Provide effort estimates, technical feasibility, and resource availability. |
| **Solution Architects** | Assess complexity, dependencies, technology fit, and required architectural effort. |
| **Enterprise / Domain Architects** | Ensure alignment with enterprise standards, reference architectures, and long-term roadmap. |
| **Security / Compliance** | Identify risks, mandatory controls, and security dependencies early. |
| **Governance / Portfolio (if applicable)** | Review alignment to investment and capacity planning. |

> **Key principle:** Intake is *jointly owned* — not a one-way request into the architecture team.

---

## Intake Process Overview

A pragmatic architecture intake process typically involves four simple steps:

### 1. Capture Demand
- Intake requests via a **single visible channel** (e.g.AHA!, Jira, Trello, or a shared form).  
- Requests can come from Product, Engineering, Security, or Architecture itself.  
- Each intake record should include:
  - Business context / objective.
  - Description of change or need.
  - Expected outcomes or value.
  - Known constraints or deadlines.
  - Requesting team / sponsor.

> Keep it brief — 5–10 structured fields max.

---

### 2. Initial Triage
- Architecture and engineering review new items weekly or bi-weekly.  
- Assess:
  - **Complexity** (e.g., low / medium / high).  
  - **Architectural touchpoints** (cross-domain, integration, data, security).  
  - **Urgency** and **business criticality**.  
  - **Readiness** (is there enough info to start?).  
- Assign **a disposition**:
  - ✅ Proceed to sizing and prioritization.  
  - 💤 Park — insufficient information.  
  - ❌ Reject — out of scope or duplicate.  

> The goal: ensure architecture focus is applied only to valuable, ready items.

---

### 3. Sizing and Effort Estimation

Sizing helps teams understand how much **architectural attention** or **engineering effort** an initiative needs.

| Sizing Category | Description | Typical Work |
|------------------|-------------|---------------|
| **Small** | Minor change, low complexity, no new tech | 1–2 hours of review or design input |
| **Medium** | Moderate complexity, single domain, known pattern | 1–2 days of architecture engagement |
| **Large** | Multi-domain, significant NFR impact, new tech or vendor | 1–2 weeks of discovery / design work |
| **Epic / Strategic** | Enterprise-scale, new platform or capability | Architecture-led discovery phase (1–4 weeks) |

**Consider dimensions such as:**
- Cross-system integration complexity.  
- Security and compliance implications.  
- Data sensitivity and regulatory constraints.  
- Technology novelty or lifecycle stage.  
- Dependency on enterprise or shared platforms.

> Use this sizing as input for **capacity planning**, not to control scope — agility is preserved by right-sizing the architectural effort, not over-planning.

---

### 4. Prioritization

After sizing, items are ranked based on **value, risk, and readiness**.

**Recommended Prioritization Criteria:**

| Dimension | Example Questions |
|------------|------------------|
| **Business Value** | Does it support a strategic product or revenue goal? |
| **Risk Reduction** | Does it reduce tech debt, security exposure, or compliance risk? |
| **Dependencies** | Does it unblock other initiatives? |
| **Readiness** | Are requirements, stakeholders, and constraints understood? |
| **Effort / Impact Ratio** | Is the value-to-effort ratio high? |
| **Time Sensitivity** | Is there a regulatory or customer deadline? |

**Prioritization should be a collaborative session** — typically a 30–60 minute conversation between Product, Architecture, Engineering, and Security leads, using a Kanban board or backlog as the shared view.

> **Output:** A prioritized and categorized backlog of architecture work (discovery, review, decision, support).

---

## Visualizing the Architecture Backlog

A simple Kanban model works well:

You can manage this in:
- **Azure DevOps Boards**
- **Jira / Confluence**
- **Trello / Notion / Airtable**
- Or even GitHub Issues + Projects

Add labels for:
- Domain (e.g., Data, Integration, Security)
- Size (S/M/L)
- Priority (High/Medium/Low)
- Requestor (Product / Eng / Security)

This makes architecture work **visible and trackable**, just like engineering work.

---

## Integrating with Product and Delivery Planning

Architecture intake shouldn’t live in isolation.  
It should tie directly into **product roadmaps** and **delivery sprints**.

### Best Practices:
- **Embed architects in sprint planning:** Review backlog items and identify where architectural engagement is needed.  
- **Align with PI Planning (if using SAFe):** Ensure architecture initiatives and enablers are represented.  
- **Connect ADO/Jira boards:** Architecture backlog should link to related product epics or features.  
- **Use lightweight design reviews:** 15–30 minute sessions instead of long-form approvals.

---

## Security and Compliance Integration

Security must be treated as a **partner in intake**, not a post-delivery reviewer.

- Include **security sign-off** on intake cards when a new pattern, data flow, or third-party system is involved.  
- Use simple tags like `SecurityImpact: High/Medium/Low`.  
- Involve security architects in prioritization when:
  - The solution handles sensitive data.
  - There are regulatory obligations (HIPAA, PCI, GDPR, etc.).
  - A new platform or vendor introduces unvetted risk.

> Integrating security early reduces later rework and accelerates compliance approval.

---

## Measuring Success

Key metrics for a healthy intake process:

| Metric | What It Shows |
|---------|----------------|
| Average time from intake to triage | Responsiveness |
| % of items correctly sized before engagement | Intake quality |
| Ratio of small vs large items | Demand balance |
| % of architecture work aligned to product priorities | Business alignment |
| Reduction in unplanned work | Predictability |

> These are indicators, not KPIs — they help improve flow, not enforce bureaucracy.

---

## Recommended Practices

1. **Keep intake transparent and accessible** — no hidden queues or side channels.  
2. **Prioritize collaboratively** — include Product, Engineering, and Security every cycle.  
3. **Size by complexity, not effort** — architects provide proportional attention.  
4. **Use Kanban, not forms** — visualize flow to spot bottlenecks.  
5. **Continuously improve** — adjust triage cadence, criteria, and visibility as teams mature.

---

## Example Cadence

| Activity | Frequency | Participants |
|-----------|------------|--------------|
| Intake triage | Weekly | Architecture, Engineering, Security |
| Prioritization session | Bi-weekly | Product, Architecture, Engineering |
| Architecture backlog review | Monthly | Broader architecture community |
| Retrospective / metrics review | Quarterly | Architecture leadership |

---

## Key Takeaways

- Intake is **how architecture stays aligned** with agile product flow.  
- Keep the process **visible, lightweight, and collaborative**.  
- Sizing ensures **right-sized effort** — not over-analysis.  
- Joint prioritization builds **trust and shared ownership**.  
- The goal isn’t control — it’s **clarity, focus, and flow**.



