# Cortex Collective

**Mine with code. Mine with ideas. Your contribution is your stake.**

> Weekly puzzle pieces across 18 planetary clusters.
> 15–30 minutes each. Use any AI tool. Every drop counts.

---

## What is CORTEX OS?

An operating system for AI agent fleets. 1,140+ specialized agents across 18 planetary clusters — each cluster owns a domain (finance, security, dev, compliance, forensics...). They observe, analyze, decide, execute, and learn as one organism.

- **1,140+ agents** across 18 clusters
- **Model-agnostic** — no vendor lock-in
- **Mathematically governed** — the Mizan balance gate ensures quality
- **Constitutional** — six Arabic-rooted principles govern every decision

**The Cortex Collective** is the human + AI collaboration layer. The agents need you.

---

## How to Join

### 1. Clone this repo

```bash
git clone https://github.com/dz31ry/cortex-collective.git
cd cortex-collective
```

This gives you the full planet structure, sample tasks, and context files. Use it as your local workbench with any AI tool you prefer.

### 2. Browse and work locally

Pick a planet that matches your skills. Open a task file. Work on it using Claude Code, Cursor, GPT, Gemini, or just your brain. The repo has instruction files for all major AI tools — they load automatically.

```bash
ls venus/tasks/          # Code tasks
ls saturn/brainstorming/  # Strategy threads
claude                    # Claude Code reads CLAUDE.md automatically
cursor .                  # Cursor reads .cursorrules automatically
```

### 3. Get your DAI server access

To submit work and collaborate with the BRAIN, email **cortex-labs.xyz@proton.me** with:
- Who are you?
- What do you do?
- What have you done before?
- Why do you want to join CORTEX?

You'll receive credentials for one of our **decentralized AI servers**:
- **Username + password** for your personal isolated terminal
- **SSH access** (any terminal, any OS) or **browser terminal** (no install needed)

```bash
# SSH into your CORTEX terminal
ssh -p YOUR_PORT worker@SERVER_IP

# Or open the browser terminal URL we send you
```

### 4. Drop your work

Inside your terminal on the DAI server, use the `drop` command to submit thoughts, completed work, decisions, and questions. The **BRAIN** (central intelligence) evaluates all contributions daily and responds in your personal briefing.

```bash
drop "your thought"                     # general thought
drop task "build cost report template"  # task
drop decision "use JSON not XML"        # decision
drop question "how does Saturn ingest?" # question
drop idea "real-time anomaly dashboard" # idea

briefing    # read your daily response from the BRAIN
```

Your terminal is pre-configured with your role context. Any AI you run inside it automatically knows what you're working on.

---

## Secure Access with Hardware Keys (Optional)

For enhanced security, we support **Nitrokey** hardware authentication. Your private SSH key lives on a physical device — even if your laptop is compromised, nobody can steal your key.

| Model | Connector | Link |
|-------|-----------|------|
| Nitrokey 3A Mini | USB-A | https://shop.nitrokey.com/shop/nk3am-nitrokey-3a-mini-116 |
| Nitrokey 3C NFC | USB-C + NFC | https://shop.nitrokey.com/shop/nk3cn-nitrokey-3c-nfc-148 |

See [NITROKEY-SETUP.md](NITROKEY-SETUP.md) for the full setup guide (macOS, Windows, Linux).

After setup, send your public key to **cortex-labs.xyz@proton.me** and we'll add it to your container. SSH with hardware key + PIN — no password needed.

---

## What Happens On The DAI Server

When you SSH into your terminal on one of our decentralized AI servers, your AI assistant automatically gets:

- **Your role context** — it knows your domain and what you're working on
- **Today's briefing** — what happened since your last session
- **Available tools** — `drop`, `thoughts`, `briefing`, `status`
- **Your workspace** — domain-specific files and references

You don't need to explain CORTEX to your AI. The context files do that automatically. Just start working.

Your terminal is fully isolated — you can't access other collaborators' data, and they can't access yours. Only the BRAIN has visibility across all terminals.

---

## Sample Tasks

Browse these to see the kind of work we need. The real tasks are in your terminal workspace.

### Codework (Code Mining)

| # | Planet | Task | Difficulty | Time |
|---|--------|------|------------|------|
| 001 | Venus | [Code Review Agent Prompt](venus/tasks/001-code-review-agent-prompt.md) | Starter | ~15 min |
| 001 | Jupiter | [Threat Classification Prompt](jupiter/tasks/001-threat-classification-prompt.md) | Starter | ~20 min |
| 001 | Mercury | [Cost Report Template](mercury/tasks/001-cost-report-template.md) | Starter | ~15 min |

### Brainstorming (Idea Mining)

| # | Topic | Time |
|---|-------|------|
| 001 | [How Will the Future Look?](brainstorming-001-the-future.md) | ~20 min |

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

## AI Tools

Use whatever AI you vibe with. Works locally with this repo AND on the DAI server.

| Tool | Locally (your clone/fork) | On DAI Server |
|------|---------------------|---------------|
| **Claude Code** | `claude` — reads CLAUDE.md | `claude` — reads CLAUDE.md + your role context + briefing |
| **Cursor** | `cursor .` — reads .cursorrules | SSH remote into your terminal |
| **Jules** | Fork repo → assign Jules → reads [JULES.md](JULES.md) | Not available on DAI server |
| **Gemini** | Paste `GEMINI.md` as context | Copy workspace context |
| **ChatGPT / GPT** | Paste task file as context | Copy workspace context |
| **Ollama** | Run locally | `sudo npm install -g ollama` on server |
| **Your Brain** | Whiteboard + paper before code. Always. | Same. |

> **Note on Jules**: Jules (Google's AI agent) cannot work directly on this repository — it requires write access. Fork or clone the repo to your own GitHub account first, then point Jules at your fork. Submit your work back via pull request.

---

## Rules

1. **One task per drop** — keep contributions focused
2. **Stay in your planet** — work within your assigned domain
3. **No secrets** — never commit keys, passwords, or internal infrastructure details
4. **Simple > clever** — code should be readable by someone who didn't write it
5. **15–30 min scope** — each puzzle piece is designed for one focused session
6. **Drops matter** — all contributions are tracked and evaluated by the BRAIN

---

## Links

- **Website**: [cortex-labs.xyz](https://cortex-labs.xyz)
- **Email**: cortex-labs.xyz@proton.me
- **Discussions**: [GitHub Discussions](https://github.com/dz31ry/cortex-collective/discussions)
- **Threema**: HN6UBSKS
- **Nitrokey (hardware keys)**: [shop.nitrokey.com](https://shop.nitrokey.com)

---

*All contributions are evaluated by the BRAIN. Your work shapes the network.*

*2026 Cortex Labs — The Cortex Collective*
