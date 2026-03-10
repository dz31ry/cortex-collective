# CLAUDE.md — Cortex Collective

## What This Repo Is

This is the **Cortex Collective** — the open collaboration layer of CORTEX OS. Contributors (humans and AI agents like Jules) solve weekly puzzle pieces across 18 planetary clusters.

## Repo Structure

```
{planet}/tasks/          — Codework puzzle pieces (code, configs, prompts)
{planet}/brainstorming/  — Strategy and architecture discussions
```

18 planets: mercury, venus, earth, mars, jupiter, saturn, uranus, neptune, pluto, ceres, eris, orion, haumea, makemake, sedna, gonggong, quaoar, orcus.

## Rules for AI Agents (Jules, Claude, etc.)

1. **Stay in your planet** — if the task is tagged `venus`, only modify files in `venus/`
2. **No secrets** — never commit API keys, passwords, internal IPs, or infrastructure details
3. **Follow the six principles** — Tabaqat (layers), Awtad (anchors), Falak (orbits), Mizan (balance), Ma' (water), Zamzam (well)
4. **Simple > clever** — code should be maintainable by humans who didn't write it
5. **One task per PR** — don't bundle unrelated changes
6. **Tests matter** — if you write code, write tests

## Planet Domains

| Planet | Domain | Focus Areas |
|--------|--------|-------------|
| Mercury | Finance & Treasury | Billing logic, cost models, ledger schemas |
| Venus | Software Dev | Code generation, static analysis, dev tooling |
| Earth | Customer Ops | User-facing workflows, onboarding, support |
| Mars | Infra & DevOps | Deployment scripts, monitoring, container configs |
| Jupiter | Security & Defense | Threat detection, access control, audit |
| Saturn | Data & Analytics | Data pipelines, OSINT, reporting |
| Uranus | R&D & Innovation | Experimental features, new architectures |
| Neptune | Compliance | Regulatory checks, documentation, governance |
| Pluto | Shadow Audit | Forensics, evidence collection, chain of custody |
| Ceres | Resources | Resource allocation, capacity planning |
| Eris | Chaos Engineering | Fault injection, resilience testing |
| Orion | Global Sync | Federation, multi-instance coordination |
| Haumea | Knowledge Synthesis | Cross-domain knowledge graphs, synthesis |
| Makemake | Edge Fleet | IoT, edge computing, lightweight agents |
| Sedna | Deep AI | Foundation models, fine-tuning, embeddings |
| Gonggong | Signal Processing | Anomaly detection, time-series analysis |
| Quaoar | Pattern Recognition | Graph analysis, pattern matching |
| Orcus | Red Team | Adversarial testing, penetration testing |
