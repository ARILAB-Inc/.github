

# arilab-platform

> 🧩 The **core blueprint** of Arilab’s CoreLab. This repo contains shared infrastructure, agent templates, documentation standards, and SDKs that power all Arilab agents and products. Every new project starts here — ensuring **consistency, scalability, and speed** across the innovation loop.

---

## 📌 Purpose

Arilab is an **iterative monetization machine**. CoreLab agents find opportunities, validate them, and GrowthLab turns them into products.
The `arilab-platform` repo is the **foundation** that makes this loop repeatable and efficient.

This repo provides:

* **Templates** → boilerplate repos for agents, services, and docs.
* **Infra** → shared IaC, Docker base, CI/CD workflows.
* **SDKs** → reusable libraries for agent communication.
* **Schemas** → standard event contracts (`OpportunityFound`, `ValidationResult`, etc.).
* **Policies** → contribution guides, security baselines, CODEOWNERS.

---

## 🏗 Repo Structure

```bash
arilab-platform/
 ├── templates/
 │    ├── agent-template/        # Boilerplate for CoreLab agents
 │    │     ├── docs/template/   # Opportunity + Validation doc templates
 │    │     ├── README.md
 │    │     ├── Dockerfile
 │    │     └── .github/workflows/ci.yml
 │    └── service-template/      # Boilerplate for product/service repos
 │
 ├── infra/
 │    ├── terraform/             # IaC baseline
 │    ├── docker-compose.base.yml
 │    └── k8s/                   # (future)
 │
 ├── agent-sdk/
 │    ├── python/                # Python SDK for agents
 │    └── node/                  # Node SDK (if needed)
 │
 ├── common-schemas/
 │    ├── opportunity_found.json
 │    └── validation_result.json
 │
 ├── CONTRIBUTING.md
 ├── CODEOWNERS
 └── README.md                   # You are here
```

---

## 🚀 How to Use

### 1. Create a New Agent Repo

* Go to **GitHub → “Use this template” → `agent-template/`**.
* Repo will auto-include:

  * `docs/opportunity.md` + `docs/validation.md`
  * Dockerfile + CI/CD workflow
  * README boilerplate

### 2. Run a 48h Validation Cycle

* Copy `/docs/template/opportunity.md` into `/docs/opportunity-cycle-1.md`.
* Run validation with **free tools + Gemini API**.
* Log outcomes in `/docs/validation.md`.

### 3. Migrate to Code (if validated)

* Use the Docker + FastAPI boilerplate.
* Connect to **Redis** (event bus) + **Postgres** (signals DB).
* Emit/consume events following **common-schemas**.

---

## 🔄 Workflow Philosophy

1. **Prototype fast** (48h cycles) using free/no-code tools.
2. **Validate** with real data + Gemini API.
3. **Migrate** to code (Langflow → Python/Docker) once proven.
4. **Deploy** using CoreLab infra (Cloud Run / Railway).
5. **Learn + Restart** → feed results into next iteration.

---

## 👥 Contribution

* Fork → branch (`feat/*`, `fix/*`, `docs/*`) → PR.
* Keep validation docs up to date (`/docs/`).
* Follow CODEOWNERS for review approvals.

---

## 📜 License

To be decided...
---

⚡ This repo is the **backbone of Arilab CoreLab** — keep it clean, simple, and reusable.
