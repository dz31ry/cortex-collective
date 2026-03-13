# Copilot / Jules Instructions — Cortex Collective

> **Jules users**: This file only works if you forked or cloned this repo to your own GitHub account. Jules cannot operate directly on the original repository. After solving a task, submit your work via pull request.

> Read this + the task file completely before writing any code.

## What You're Working On

This is the **Cortex Collective** — the open collaboration layer of CORTEX OS, an operating system for AI agent fleets (1,140+ agents, 18 planetary clusters, model-agnostic, constitutionally governed).

You are solving **puzzle pieces** — scoped tasks (15-30 min) that contribute to the system.

## Critical Rules

1. **Stay in your planet** — if the task says `venus`, only create/modify files in `venus/`
2. **No secrets** — never generate API keys, passwords, internal IPs, or infrastructure details
3. **Model-agnostic** — never write prompts or code that only works with one LLM
4. **One task per PR** — solve exactly the task described, nothing more
5. **Meet ALL acceptance criteria** — every task has a checklist, satisfy every item
6. **Simple > clever** — readable code over elegant code

## Six Principles

Reference these in your work where the task mentions them:

- **Tabaqat** (Layers) — hierarchical organization, each agent has a scope
- **Awtad** (Anchors) — stability, recovery, failsafes
- **Falak** (Orbits) — isolation between domains, no data leaks
- **Mizan** (Balance) — cost vs. quality, not too much, not too little
- **Ma'** (Water) — collective knowledge flows and is shared
- **Zamzam** (Well) — verified truth, quality-scored at source

## How Agents Work

Agents receive structured messages → process using their system prompt → produce structured output (classification, recommendation, report, or code). When writing agent prompts, define: identity, input format, output format, severity levels, and governing principle(s).

## Planet Domains

Mercury=Finance, Venus=Dev, Earth=Ops, Mars=Infra, Jupiter=Security, Saturn=Data, Uranus=R&D, Neptune=Compliance, Pluto=Audit, Ceres=Resources, Eris=Chaos, Orion=Federation, Haumea=Knowledge, Makemake=Edge, Sedna=DeepAI, Gonggong=Signals, Quaoar=Patterns, Orcus=RedTeam

## Output Quality

- Under word limits specified in the task
- Clean formatting (markdown for docs, plain text for prompts)
- Placeholder data where specified (never use real data)
- Test your output mentally — would this actually work in production?
