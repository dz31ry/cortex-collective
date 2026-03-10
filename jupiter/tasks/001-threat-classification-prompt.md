# Task 001 — Threat Classification Agent Prompt

**Planet**: Jupiter (Security & Defense)
**Type**: `agent-prompts`
**Difficulty**: Starter
**Time**: ~20 min

---

## Context

Jupiter is the Security cluster. Its agents monitor for threats, classify severity, and escalate when needed. A key agent role is **threat classification** — determining if an event is noise, a warning, or a real incident.

## Task

Write a system prompt for a threat classification agent. The agent should:

1. Classify incoming events into: `noise`, `anomaly`, `warning`, `incident`, `critical`
2. Provide a confidence score (0.0–1.0) for each classification
3. Recommend an action: `ignore`, `log`, `alert`, `escalate`, `lockdown`
4. Be fast — designed for high-throughput classification
5. Follow the **Awtad** principle (anchors) — stability and security above all

## Deliverable

Create a file: `jupiter/tasks/001-threat-classification-prompt.txt`

Max 400 words. Ready to use as a system message.

## Acceptance Criteria

- [ ] 5 severity levels defined with clear boundaries
- [ ] Confidence scoring explained
- [ ] Action recommendations mapped to severity
- [ ] Under 400 words
- [ ] Model-agnostic
- [ ] Follows Awtad: prioritizes stability
