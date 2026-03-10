# Task 001 — Code Review Agent Prompt

**Planet**: Venus (Software Dev)
**Type**: `agent-prompts`
**Difficulty**: Starter
**Time**: ~15 min

---

## Context

CORTEX OS has a Venus cluster dedicated to Software Development. Venus agents handle code generation, static analysis, dev tooling, and **code review**.

### How Code Review Works in CORTEX OS

When a developer (human or AI) submits code, a code review agent receives:
- A **code diff** (unified diff format — lines added/removed)
- Optional **file context** (surrounding code for understanding)
- The **language** and **framework** involved

The agent must analyze the diff and produce a **structured review** — a list of findings, each with a severity level and a brief explanation. The review goes back to the developer for action.

### What Makes a Good Agent Prompt

Agent prompts in CORTEX OS are **system messages** — they set the agent's identity, behavior, and output format. A good prompt:
- Clearly defines the agent's role and scope
- Specifies what input it expects
- Specifies what output format to produce
- Includes a severity/priority framework
- References the governing principle (for this agent: **Mizan** — balance)
- Works with ANY LLM — no model-specific instructions

### The Mizan Principle (Balance)

Mizan means "the balance" — cost vs. quality, enforced mathematically. For code review, this means:
- Don't over-flag (marking everything as a problem wastes developer time)
- Don't under-flag (missing real bugs is worse than being annoying)
- Flag **real issues**, not style preferences
- Severity must be proportional — a typo in a comment is not "critical"

## Task

Write a system prompt for a code review agent. The agent should:

1. Review code diffs for bugs, security issues, and logic errors
2. Prioritize findings by severity: `critical` → `high` → `medium` → `low`
3. Be concise — no fluff, no filler, no praise
4. Flag only real issues, not style preferences
5. Follow the **Mizan** principle — balanced, not over-zealous

### Example Output Format (Suggest Something Like This)

```
[CRITICAL] Line 42: SQL injection — user input concatenated into query string
[HIGH] Line 87: Race condition — shared state modified without lock
[MEDIUM] Line 15: Null check missing — will throw if response is empty
[LOW] Line 103: Magic number — consider naming this constant
```

## Deliverable

Create a file: `venus/tasks/001-code-review-prompt.txt`

The prompt should be ready to use as a system message for an LLM. Max 500 words.

## Acceptance Criteria

- [ ] Prompt covers: bugs, security, logic errors, performance
- [ ] Severity levels defined (critical, high, medium, low) with clear boundaries
- [ ] Output format specified (structured findings, not prose)
- [ ] Concise — under 500 words
- [ ] No model-specific instructions (must work with any LLM)
- [ ] Follows Mizan: balanced, not over-zealous
- [ ] Agent identity clearly defined (who am I, what do I do)
