# CLAUDE.md — Cortex Collective

> Read this before working on any task. This is your context.

## What is CORTEX OS?

CORTEX OS is an operating system for AI agent fleets. 1,140+ specialized agents organized into 18 planetary clusters, each owning a domain (finance, security, dev, compliance, forensics, etc.). The agents observe, analyze, decide, execute, and learn as one organism.

Key concepts you need to understand:

- **Agents** are specialized AI workers. Each has a callsign (e.g. GUARDIAN, AUDITOR, SENTINEL-1), belongs to a cluster, operates at a specific layer, and has a defined role. Agents communicate through structured message channels.
- **Clusters** are planet-named domains. Mercury = Finance. Jupiter = Security. Venus = Dev. Each cluster has ~60 agents with different specializations.
- **Layers** follow the Tabaqat principle — 7 hierarchical levels from strategic command (BRAIN) down to raw execution. Higher layers coordinate, lower layers execute.
- **Model-agnostic** means agents work with ANY LLM (Claude, GPT, Gemini, Llama, Mistral, local models). Prompts must never be model-specific.
- **Constitutional governance** — six principles (below) govern every agent decision. Not guidelines — hard rules enforced by the system.

## Six Principles

These are non-negotiable. Reference them in your work.

| Principle | Arabic | Meaning | In Practice |
|-----------|--------|---------|-------------|
| **Tabaqat** | الطبقات | The Seven Layers | Hierarchical authority — each agent knows its layer and scope |
| **Awtad** | الأوتاد | The Anchors | Stability first — failsafes, recovery, security pegs that hold the system |
| **Falak** | الفلك | The Orbits | Isolation — each cluster stays in its orbit, data doesn't leak between domains |
| **Mizan** | الميزان | The Balance | Cost vs. quality gate — not too much, not too little, mathematically enforced |
| **Ma'** | الماء | The Water | Collective knowledge — learning flows and is shared across the organism |
| **Zamzam** | زمزم | The Well | Verified truth — all knowledge is quality-scored at source, no hallucinations |

## Repo Structure

```
{planet}/tasks/          — Codework puzzle pieces (code, configs, prompts)
{planet}/brainstorming/  — Strategy and architecture discussions
```

18 planets: mercury, venus, earth, mars, jupiter, saturn, uranus, neptune, pluto, ceres, eris, orion, haumea, makemake, sedna, gonggong, quaoar, orcus.

## Rules for AI Agents

1. **Stay in your planet** — if the task is tagged `venus`, only modify files in `venus/`
2. **No secrets** — never commit API keys, passwords, internal IPs, or infrastructure details
3. **Follow the six principles** — reference them explicitly in your work
4. **Simple > clever** — code should be maintainable by humans who didn't write it
5. **One task per drop** — keep contributions focused
6. **Tests matter** — if you write code, write tests
7. **Model-agnostic** — never write prompts or code that only works with one LLM
8. **Read the full task** — every task has Context, Task, Deliverable, and Acceptance Criteria. Meet ALL criteria.

## Planet Domains

| Planet | Domain | Focus Areas |
|--------|--------|-------------|
| Mercury | Finance & Treasury | Billing logic, cost models, ledger schemas, budget tracking |
| Venus | Software Dev | Code review, static analysis, dev tooling, CI/CD prompts |
| Earth | Customer Ops | User-facing workflows, onboarding, support automation |
| Mars | Infra & DevOps | Deployment scripts, monitoring, alerting, container configs |
| Jupiter | Security & Defense | Threat detection, access control, audit, incident response |
| Saturn | Data & Analytics | Data pipelines, reporting, intelligence, OSINT |
| Uranus | R&D & Innovation | Experimental features, new architectures, proof-of-concepts |
| Neptune | Compliance | Regulatory checks, governance docs, policy templates |
| Pluto | Shadow Audit | Forensics, evidence collection, chain of custody |
| Ceres | Resources | Resource allocation, capacity planning, optimization |
| Eris | Chaos Engineering | Fault injection, resilience testing, failure scenarios |
| Orion | Global Sync | Federation protocols, multi-instance coordination |
| Haumea | Knowledge Synthesis | Cross-domain knowledge graphs, synthesis documents |
| Makemake | Edge Fleet | IoT, edge computing, lightweight agent configs |
| Sedna | Deep AI | Foundation models, fine-tuning, embeddings, model eval |
| Gonggong | Signal Processing | Anomaly detection, time-series analysis, alerting |
| Quaoar | Pattern Recognition | Graph analysis, pattern matching, behavioral analysis |
| Orcus | Red Team | Adversarial testing, penetration testing, attack simulation |

## How Agents Work (For Prompt Writers)

When writing agent prompts, understand the flow:

```
Input → Agent receives a structured message (text, data, or event)
Process → Agent analyzes using its system prompt + context
Output → Agent produces a structured response (classification, recommendation, report, or code)
```

Agent prompts should:
- Define the agent's identity and scope clearly
- Specify input format expectations
- Specify output format expectations
- Include severity/priority frameworks where applicable
- Reference which principle(s) govern this agent's decisions
- Be under 500 words unless the task specifies otherwise

## How This Repo Works

This repo is a **local workbench** — clone it for the planet structure, sample tasks, and AI instruction files. The real collaboration happens on our **decentralized AI servers (DAI)**.

To get access: email **cortex-labs@proton.me** with your name, expertise, and which planet(s) interest you. You'll receive a username, password, and SSH access to your own isolated terminal. From there, use the `drop` command to submit your work — the BRAIN evaluates all contributions daily.

For hardware-backed SSH authentication (optional), see [NITROKEY-SETUP.md](NITROKEY-SETUP.md).
