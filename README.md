# 🧩 AriLab Agents – Team Guide

AriLab is not about building one product, it’s about building a **system of agents** that continuously discover, validate, and monetize opportunities.  

To avoid confusion, here’s how we’ll work with agents phase by phase.

---

## 🔄 Phase 1: No-Code Prototyping (48h validation cycles)

**Goal:** Fastest way to test if an agent idea works.  

**Tools:**  
- n8n (automation workflows)  
- Zapier / Make (if needed)  
- Dify.ai / Langflow (for quick AI agent logic)  

**Process:**  
1. Each agent starts as a no-code workflow.  
2. Validate in 48h cycles (does it work, add value, give usable output?).  
3. Document results in `docs/opportunity.md` + `docs/validation.md`.  

**Examples:**  
- Market Research Agent = n8n workflow that scrapes Reddit + saves results to Google Sheets.  
- Monetization Agent = Zapier workflow that calculates basic revenue estimates from sample data.  

👉 If it fails, we **iterate or kill fast**. If it works, we move to **Phase 2**.  

---

## ⚙️ Phase 2: Code-based Agents (scalable, reusable)

**Goal:** Turn validated no-code agents into proper coded microservices.  

**Stack:**  
- Python (FastAPI / LangChain / custom scripts)  
- Node.js (for certain integrations)  
- Containerized with Docker  

**Process:**  
1. Start from `arilab-platform` templates (agent scaffold).  
2. Move logic from no-code tool → codebase.  
3. Add unit tests + CI/CD pipelines.  
4. Deploy lightweight versions (Cloud Run / Railway).  

**Repo Workflow:**  
- Each agent has its own repo under the org.  
- Devs work in branches → raise Pull Requests.  
- PRs must include updates to `/docs/validation.md` with test results.  

---

## 🚀 Phase 3: Integration into CoreLab

**Goal:** Connect agents into a system.  

**Infra:**  
- Event bus (Redis / PubSub)  
- Shared schemas (e.g., OpportunityFound, ValidationResult)  
- Observability (Grafana dashboards)  

**Process:**  
1. Agents publish/consume events, not just act alone.  
2. CoreLab dashboard shows outputs & impact of each agent.  
3. Feedback loop ensures learnings flow into the next cycle.  

---

## 📌 Team Expectations

- Every agent **starts no-code**. Don’t jump to coding until validated.  
- **Document everything.** Use `opportunity.md` and `validation.md`.  
- Work in **pairs (2-person pods)**. Each pod owns one agent per cycle.  
- **Pull Requests = source of truth.** All work must go through GitHub with PRs for review.  

---

## ✅ Example Flow

1. Lanre + Vishnu take Market Research Agent.  
2. They build it in n8n → outputs top 10 AI startup trends from Twitter.  
3. They log validation in `docs/validation.md`.  
4. Team approves → they move to coded version (Python + FastAPI).  
5. Repo gets PR → reviewed → merged.  
6. Later, the agent is plugged into CoreLab.  

---

## 🗺️ Phased Workflow (Visual Overview)

```mermaid
flowchart TD
  A[Gemini / ChatGPT] -->|One-off answers| B[Why not enough?]
  B --> C[Nuance · Persistence · Orchestration · Action · Moat]

  subgraph AGENTS[🧩 AriLab Agent Workflow]
    D[🔄 Phase 1: No-Code Prototype<br>(48h validation cycles)]
    E[⚙️ Phase 2: Code-based Agent<br>(scalable + reusable)]
    F[🚀 Phase 3: CoreLab Integration<br>(system of agents)]
  end

  C --> D
  D --> E
  E --> F
  F --> G[🌍 Impact → Ventures · Insights · Real-World Change]

```
---

🏁 Summary

Phase 1 = fast + no-code (prove it works).

Phase 2 = coded + reusable (make it scalable).

Phase 3 = integrated (becomes part of CoreLab engine).


✨ AriLab’s strength isn’t just ideas. It’s the system that turns ideas into impact.

