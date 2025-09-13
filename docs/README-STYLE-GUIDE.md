# 📘 Arilab README Style Guide

This guide defines the **standard README format** for all Arilab repositories.
Every repo should follow this structure to ensure clarity and consistency.

---

## 1. Title & Tagline

```md
# <Repo-Name>  

> 🎯 One-line description of what this repo does and why it exists.  
```

Example:

```md
# Market-Research-Agent  

> 🔎 Identifies emerging market opportunities by scanning the web, competitors, and social feeds.  
```

---

## 2. Purpose

```md
## 📌 Purpose  

- Short bullet points explaining the role of this repo.  
- What problems it solves.  
- Which other agents/repos it interacts with.  
```

---

## 3. Workflow

```md
## 🔄 Workflow  

### Phase 1: No-Code Validation (48h cycles)  
- State which free / no-code tools are used.  
- Show how validation cycles are logged (`/docs/opportunity.md`, `/docs/validation.md`).  
- Decision options: Continue / Modify / Discard.  

### Phase 2: Coded Agent (if validated)  
- Mention the coding language, Docker, infra setup.  
- Specify event bus (Redis), schemas, or outputs.  
```

---

## 4. Repo Structure

````md
## 📂 Repo Structure  

```bash
<Repo-Name>/
 ├── docs/
 │    ├── template/        # Templates from arilab-platform
 │    │    ├── opportunity.md
 │    │    ├── validation.md
 │    ├── opportunity-cycle-1.md
 │    ├── validation.md
 │
 ├── src/                  # Code version (after validation)
 │
 ├── Dockerfile            # From arilab-platform
 ├── README.md             # You are here
 └── .github/
      └── ISSUE_TEMPLATE/
           └── validation-cycle.md
````

````

---

## 5. Contribution Guidelines  

```md
## ✅ Contribution Guidelines  

- Start with **no-code validation** (48h cycles).  
- Only write code if the project passes validation.  
- Log everything in `/docs/`.  
- Follow [CONTRIBUTING.md](https://github.com/ARILAB-Inc/arilab-platform/blob/main/CONTRIBUTING.md).  
````

---

## 6. License

```md
## 📜 License  
To be decided.  
```

(Or MIT/Apache/etc. when you choose.)

---

## ⚡ Reminder Footer

End each README with a **short mantra/reminder**:

```md
⚡ Reminder: **Validate fast → then build in code.**  
```

---

✅ With this guide:

* Every repo looks familiar to contributors.
* Onboarding new developers becomes trivial.
* Repos reflect Arilab’s **“Validate fast → Build later”** philosophy.
