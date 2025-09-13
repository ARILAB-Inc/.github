# Contributing to Arilab

Thank you for contributing to **Arilab CoreLab** 🚀
We follow a **fast-validation → code → deploy** philosophy. Please read this guide before opening PRs.

---

## 🏗 Branching Model

* **Default branch:** `main` → production-ready only.
* **Development branches:**

  * `feat/*` → new features (e.g., `feat/scraper-agent`)
  * `fix/*` → bug fixes (e.g., `fix/typo-docs`)
  * `docs/*` → documentation changes
  * `infra/*` → infra changes (CI/CD, Docker, Terraform)

👉 Always branch from `main`. Keep branches **short-lived**.

---

## 🔄 Pull Request Workflow

1. **Open a PR** against `main`.

   * Title: `[feat] Add scraper pipeline`
   * Link to related issue (if any).

2. **Checks required before merge:**

   * ✅ Linting & type checks
   * ✅ Unit tests
   * ✅ Security scans (Dependabot, CodeQL)
   * ✅ Docs updated (if cycle-related)

3. **Review process:**

   * At least **1 review** required (2 if core infra).
   * System Architect has final say for infra/SDK changes.

4. **Preview deploys:**

   * Every PR spins up a **preview environment** (Cloud Run / Railway).
   * Validate changes before merging.

---

## 📊 Validation Cycle Rules (48h)

Every new idea or agent must go through a **48-hour validation cycle** before scaling.

1. Copy `/docs/template/opportunity.md` → `/docs/opportunity-cycle-X.md`.
2. Run validation using **free tools + Gemini API** (no-code/low-code first).
3. Log outcome in `/docs/validation.md`.
4. Open a GitHub Issue with template **“Run Validation Cycle”**.
5. At end of cycle, mark issue as:

   * ✅ Continue → migrate to code-based agent
   * ⚠️ Modify → retry with adjustments
   * ❌ Discard → log learnings

⚡ **No code is written until validation cycle passes**.

---

## 🧪 Testing

* Use `pytest` (Python) or equivalent for other stacks.
* Unit tests must cover new features.
* ML agents should include a **small evaluation harness** for reproducibility.

---

## 📦 Releases

* Tag releases as `vX.Y.Z`.
* Each release must:

  * Auto-deploy to staging
  * Pass integration tests
  * Generate SBOM + security scan
* Production deploys happen only after staging passes.

---

## 🛡 Code of Conduct

* Respect collaboration.
* Document your work clearly.
* Share validation learnings — failures are valuable.

---

## ✅ Summary

* **Branch smart** (`feat/*`, `fix/*`, `docs/*`).
* **PRs must pass checks + review.**
* **Validate every idea in 48h cycles.**
* **Keep CoreLab clean + consistent.**
