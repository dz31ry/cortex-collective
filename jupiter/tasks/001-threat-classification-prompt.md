# Task 001 — Threat Classification Agent Prompt

**Planet**: Jupiter (Security & Defense)
**Type**: `agent-prompts`
**Difficulty**: Starter
**Time**: ~20 min

---

## Context

Jupiter is the Security & Defense cluster of CORTEX OS. Its agents monitor for threats across the entire ecosystem — all 18 planet clusters report security events to Jupiter.

### How Threat Classification Works

Jupiter receives a constant stream of **security events** from other clusters. Examples:

- Venus (Dev) reports: "3 failed login attempts from unknown IP in 2 minutes"
- Mercury (Finance) reports: "Unusual billing spike — 400% increase in API costs for agent ANALYST-7"
- Mars (Infra) reports: "Container restart loop detected on monitoring service"
- Saturn (Data) reports: "Data export request for 50,000 records from unrecognized source"
- Earth (Ops) reports: "Customer reported receiving email they didn't request"

Most of these are **noise** — normal operations that look unusual. Some are **real threats** that need immediate action. The threat classification agent must tell the difference, fast.

### The Awtad Principle (Anchors)

Awtad means "the anchors" or "the pegs" — the things that keep the tent standing in a storm. For security, this means:
- **Stability above all** — when in doubt, protect the system
- **Fail safe** — if classification is uncertain, escalate rather than ignore
- **Recovery-ready** — every response should include a recommended action
- **No single point of failure** — the agent's output feeds multiple downstream systems

### What Makes a Good Agent Prompt

Agent prompts are system messages that define behavior. For a classification agent:
- Define clear **input expectations** (what does an event look like?)
- Define clear **output format** (classification + confidence + action)
- Define clear **severity boundaries** (when does "anomaly" become "incident"?)
- Be designed for **high throughput** — this agent processes hundreds of events per hour

## Task

Write a system prompt for a threat classification agent. The agent should:

1. Classify incoming events into 5 levels: `noise`, `anomaly`, `warning`, `incident`, `critical`
2. Provide a confidence score (0.0–1.0) for each classification
3. Recommend an action: `ignore`, `log`, `alert`, `escalate`, `lockdown`
4. Be fast — designed for high-throughput classification, no verbose reasoning
5. Follow the **Awtad** principle — stability and security above all

### Severity Boundaries (Guide)

| Level | Meaning | Example |
|-------|---------|---------|
| `noise` | Normal operation, no concern | Scheduled restart, routine log rotation |
| `anomaly` | Unusual but not threatening | Slight traffic spike during business hours |
| `warning` | Potentially harmful, needs monitoring | Multiple failed logins from one IP |
| `incident` | Active threat, immediate response needed | Unauthorized data access detected |
| `critical` | System integrity at risk | Active data exfiltration, privilege escalation |

### Example Output Format

```
CLASSIFICATION: warning
CONFIDENCE: 0.82
ACTION: alert
REASONING: 3 failed logins from unknown IP in 2 minutes suggests brute-force attempt.
Pattern matches known credential-stuffing behavior but volume is low.
Recommend monitoring + rate limiting.
```

## Deliverable

Create a file: `jupiter/tasks/001-threat-classification-prompt.txt`

Max 400 words. Ready to use as a system message.

## Acceptance Criteria

- [ ] 5 severity levels defined with clear boundaries between each
- [ ] Confidence scoring explained (what makes 0.9 vs 0.5?)
- [ ] Action recommendations mapped to severity levels
- [ ] Under 400 words
- [ ] Model-agnostic (works with any LLM)
- [ ] Follows Awtad: when uncertain, escalate rather than ignore
- [ ] High-throughput design: concise output, no verbose reasoning
- [ ] Agent identity clearly defined
