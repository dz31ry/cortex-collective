# Cortex Collective

**Mine with code. Mine with ideas. Your contribution is your stake.**

> Weekly puzzle pieces across 18 planetary clusters.
> 15–30 minutes each. Use any AI tool. Every commit counts.

---

## What is CORTEX OS?

An operating system for AI agent fleets. 1,140+ specialized agents across 18 planetary clusters — each cluster owns a domain (finance, security, dev, compliance, forensics...). They observe, analyze, decide, execute, and learn as one organism.

- **1,140+ agents** across 18 clusters
- **Model-agnostic** — no vendor lock-in
- **Mathematically governed** — the Mizan balance gate ensures quality
- **Constitutional** — six Arabic-rooted principles govern every decision

**The Cortex Collective** is the human + AI collaboration layer. The agents need you.

---

## Quick Start

```bash
git clone https://github.com/dz31ry/cortex-collective.git
cd cortex-collective

# Browse planets and pick your domain
ls venus/tasks/          # Code tasks
ls saturn/brainstorming/  # Strategy threads

# Use your preferred AI tool
claude                    # Claude Code — conversational
cursor .                  # Cursor — AI-assisted editor
# or just open in any editor

# Solve → Commit → PR
git checkout -b my-contribution
# ... do the work ...
git add . && git commit -m "venus: solve task 001"
git push origin my-contribution
# Open PR on GitHub
```

---

## How It Works

### Codework (Code Mining)

```
┌─────────────────────────────────────────────────────────┐
│                    CODEWORK FLOW                        │
│                                                         │
│   Browse Tasks ──→ Pick Planet ──→ Clone Repo           │
│        │                              │                 │
│        ▼                              ▼                 │
│   Read Task Brief          Use Your AI Tool             │
│   (15-30 min scope)        (Claude/Cursor/Gemini/Jules) │
│        │                              │                 │
│        ▼                              ▼                 │
│   Write Solution ◄────────── AI Assists You             │
│        │                                                │
│        ▼                                                │
│   Open PR ──→ Review ──→ Merge ──→ deAI Evaluation      │
└─────────────────────────────────────────────────────────┘
```

**Task types**: `agent-prompts` · `migrations` · `tools` · `daemons` · `frontend` · `infra` · `tests` · `docs`

### Brainstorming (Idea Mining)

```
┌─────────────────────────────────────────────────────────┐
│                  BRAINSTORMING FLOW                     │
│                                                         │
│   Browse Threads ──→ Pick Planet ──→ Read Context       │
│        │                                │               │
│        ▼                                ▼               │
│   Think (15-30 min)            Reference Principles     │
│        │                       (Tabaqat/Awtad/Falak/    │
│        ▼                        Mizan/Ma'/Zamzam)       │
│   Write Response ◄──────────────────────┘               │
│        │                                                │
│        ▼                                                │
│   Submit via PR or Discussion ──→ deAI Evaluation       │
└─────────────────────────────────────────────────────────┘
```

---

## Vibe Coding Stack

Use whatever AI tools you vibe with. The Collective is tool-agnostic.

Each tool reads its own instruction file automatically:

| Tool | Instruction File | How to Use |
|------|-----------------|------------|
| **Claude Code** | `CLAUDE.md` | `clone → cd → claude → "solve venus task 001"` |
| **Cursor** | `.cursorrules` | `clone → cursor . → open task → AI assists` |
| **Jules** | `.github/copilot-instructions.md` | `create issue → @jules solve this → review PR` |
| **Gemini** | `GEMINI.md` | `paste GEMINI.md as context → upload task → write solution` |
| **Windsurf / Copilot** | `.cursorrules` / `.github/copilot-instructions.md` | `open repo → AI assists → commit` |
| **Your Brain** | `README.md` | **Whiteboard + paper before code. Always.** |

Every AI tool gets full context about CORTEX OS, the 6 principles, planet domains, and rules — automatically.

---

## The 18 Planets

Each planet owns a domain. Pick the one that fits your skills.

### Inner Planets (Core Operations)

| Planet | Domain | You'll Work On |
|--------|--------|----------------|
| **Mercury** | Finance & Treasury | Billing logic, cost models, budget templates, efficiency metrics |
| **Venus** | Software Dev | Code review prompts, dev tooling, static analysis configs |
| **Earth** | Customer Ops | User workflows, onboarding flows, support automation |
| **Mars** | Infra & DevOps | Deployment scripts, monitoring configs, CI templates |

### Middle Planets (Specialized Systems)

| Planet | Domain | You'll Work On |
|--------|--------|----------------|
| **Jupiter** | Security & Defense | Threat classification, access control rules, audit prompts |
| **Saturn** | Data & Analytics | Data pipeline designs, reporting templates, OSINT tools |
| **Uranus** | R&D & Innovation | Experimental architectures, proof-of-concepts, new patterns |
| **Neptune** | Compliance | Regulatory checklists, governance docs, policy templates |

### Outer Planets (Advanced Operations)

| Planet | Domain | You'll Work On |
|--------|--------|----------------|
| **Pluto** | Shadow Audit | Forensics prompts, evidence chain templates, audit trails |
| **Ceres** | Resources | Capacity planning models, resource allocation logic |
| **Eris** | Chaos Engineering | Fault injection configs, resilience test plans |
| **Orion** | Global Sync | Federation protocols, multi-instance coordination |

### Kuiper Belt (Frontier)

| Planet | Domain | You'll Work On |
|--------|--------|----------------|
| **Haumea** | Knowledge Synthesis | Knowledge graph schemas, cross-domain synthesis |
| **Makemake** | Edge Fleet | Lightweight agent configs, IoT integration |
| **Sedna** | Deep AI | Fine-tuning strategies, embedding pipelines, model evaluation |
| **Gonggong** | Signal Processing | Anomaly detection rules, time-series analysis |
| **Quaoar** | Pattern Recognition | Graph analysis configs, pattern matching logic |

### Trans-Kuiper (Adversarial)

| Planet | Domain | You'll Work On |
|--------|--------|----------------|
| **Orcus** | Red Team | Adversarial test cases, penetration testing prompts |

---

## Repo Structure

```
cortex-collective/
├── mercury/
│   ├── tasks/              ← Codework puzzle pieces
│   │   └── 001-cost-report-template.md
│   ├── brainstorming/      ← Strategy discussions
│   └── README.md           ← Planet overview
├── venus/
│   ├── tasks/
│   │   └── 001-code-review-agent-prompt.md
│   ├── brainstorming/
│   └── README.md
├── jupiter/
│   ├── tasks/
│   ├── brainstorming/
│   └── README.md
├── ... (18 planets total)
├── CLAUDE.md               ← Instructions for AI agents
└── README.md               ← You are here
```

---

## Six Guiding Principles

Every contribution — code or ideas — operates within these principles.

| | Name | Meaning | Applied To |
|---|------|---------|------------|
| الطبقات | **Tabaqat** (Layers) | Hierarchical organization — 7 layers from hardware to consciousness | Architecture decisions, system design |
| الأوتاد | **Awtad** (Anchors) | Stability, recovery, security — the pegs that hold the tent | Error handling, failsafes, rollback |
| الفلك | **Falak** (Orbits) | Isolation and routing — each planet stays in its orbit | Domain boundaries, data flow |
| الميزان | **Mizan** (Balance) | Cost control, quality gating — not too much, not too little | Code review thresholds, budget limits |
| الماء | **Ma'** (Water) | Collective knowledge, learning — flowing and shared | Knowledge synthesis, documentation |
| زمزم | **Zamzam** (Well) | Verified truth, quality scoring — the source must be pure | Data validation, source verification |

---

## Task Types

| Tag | What | Example |
|-----|------|---------|
| `agent-prompts` | Agent behavior and reasoning prompts | Write a code review agent system prompt |
| `migrations` | Schema evolution and data structures | Design a billing ledger schema |
| `tools` | Tool integrations for any planet | Build a SAST scanner config |
| `daemons` | Background automation and scheduling | Design a log rotation schedule |
| `frontend` | UI components and visualizations | Build a cluster health dashboard |
| `infra` | Deployment and configuration | Write a monitoring alert template |
| `tests` | Automated testing | Create edge-case test suites |
| `docs` | Architecture and operational docs | Document a data flow diagram |

---

## Current Puzzle — Week 01

### Codework

| # | Planet | Task | Difficulty | Time |
|---|--------|------|------------|------|
| 001 | Venus | [Code Review Agent Prompt](venus/tasks/001-code-review-agent-prompt.md) | Starter | ~15 min |
| 001 | Jupiter | [Threat Classification Prompt](jupiter/tasks/001-threat-classification-prompt.md) | Starter | ~20 min |
| 001 | Mercury | [Cost Report Template](mercury/tasks/001-cost-report-template.md) | Starter | ~15 min |

### Brainstorming

| # | Planet | Topic | Time |
|---|--------|-------|------|
| 001 | Saturn | [Data Pipeline Architecture](saturn/brainstorming/001-data-pipeline-architecture.md) | ~15 min |
| 001 | — | [How Will the Future Look?](brainstorming-001-the-future.md) | ~20 min |

---

## Rules

1. **One task per PR** — don't bundle unrelated work
2. **Stay in your planet** — if the task says `venus`, work in `venus/`
3. **No secrets** — never commit keys, passwords, internal infrastructure details
4. **Simple > clever** — code should be readable by someone who didn't write it
5. **15–30 min scope** — each puzzle piece is designed for one focused session
6. **Commits matter** — all contributions are tracked and evaluated for the deAI network

---

## Links

- **Website**: [cortex-labs.xyz](https://cortex-labs.xyz)
- **Collective Page**: [cortex-labs.xyz/collective](https://cortex-labs.xyz/collective)
- **Discussions**: [GitHub Discussions](https://github.com/dz31ry/cortex-collective/discussions)
- **Email**: cortex-labs.xyz@proton.me
- **Threema**: HN6UBSKS

---

*All commits are evaluated for the decentralized AI network.*

*2026 Cortex Labs — The Cortex Collective*
