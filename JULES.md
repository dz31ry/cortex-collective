# JULES.md — Cortex Collective

> **Important**: Jules cannot operate directly on this repository. You must **fork** or **clone** it to your own GitHub account first. After solving a task, submit your work back via **pull request**.

## What is CORTEX OS?

An operating system for AI agent fleets. 1,140+ specialized agents organized into 18 planetary clusters. Each cluster owns a domain — Finance (Mercury), Security (Jupiter), Software Dev (Venus), Data (Saturn), and 14 more. Agents observe, analyze, decide, execute, and learn as one organism.

**Key properties:**
- **Model-agnostic** — works with any LLM (Claude, GPT, Gemini, Llama, Mistral, local models)
- **Constitutional governance** — 6 Arabic-rooted principles are hard rules, not guidelines
- **Collective** — humans + AI agents collaborate through weekly puzzle pieces

## Six Principles (Reference These)

| Principle | Meaning | Applied To |
|-----------|---------|------------|
| **Tabaqat** (Layers) | Hierarchical organization — 7 levels from command to execution | Architecture, scope boundaries |
| **Awtad** (Anchors) | Stability, recovery, failsafes | Error handling, security |
| **Falak** (Orbits) | Isolation between domains — no data leaks | Domain boundaries, routing |
| **Mizan** (Balance) | Cost vs. quality — mathematically enforced | Review thresholds, budgets |
| **Ma'** (Water) | Collective knowledge — flows and is shared | Documentation, learning |
| **Zamzam** (Well) | Verified truth — quality-scored at source | Data validation, fact-checking |

## How to Work on Tasks

1. Read the full task file (Context, Task, Deliverable, Acceptance Criteria)
2. Stay in the planet directory specified — if the task says `venus`, only touch `venus/`
3. Meet ALL acceptance criteria — every task has a checklist
4. Keep under word/size limits specified in the task
5. Reference principles where the task mentions them
6. Never include secrets, keys, passwords, or infrastructure details
7. Write model-agnostic solutions — no LLM-specific code

## Planet Domains

Mercury=Finance, Venus=Dev, Earth=Ops, Mars=Infra, Jupiter=Security, Saturn=Data, Uranus=R&D, Neptune=Compliance, Pluto=Audit, Ceres=Resources, Eris=Chaos, Orion=Federation, Haumea=Knowledge, Makemake=Edge, Sedna=DeepAI, Gonggong=Signals, Quaoar=Patterns, Orcus=RedTeam

## Workflow

```
1. Fork this repo to your GitHub account
2. Assign Jules to a task issue in YOUR fork
3. Jules reads this file + the task file automatically
4. Review Jules' PR in your fork
5. Submit a PR back to the original repo
```

## Output Quality

- Clean formatting (markdown for docs, plain text for prompts)
- Placeholder data where specified (never use real data)
- Simple > clever — code should be readable by someone who didn't write it
- One task per PR — don't bundle unrelated changes
