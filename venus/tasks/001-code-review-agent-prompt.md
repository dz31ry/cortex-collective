# Task 001 — Code Review Agent Prompt

**Planet**: Venus (Software Dev)
**Type**: `agent-prompts`
**Difficulty**: Starter
**Time**: ~15 min

---

## Context

CORTEX OS has a Venus cluster dedicated to Software Development. One of its key roles is **code review** — agents that review PRs, flag issues, and suggest improvements.

## Task

Write a system prompt for a code review agent. The agent should:

1. Review code diffs for bugs, security issues, and style problems
2. Prioritize findings by severity (critical → low)
3. Be concise — no fluff, no filler
4. Flag only real issues, not style preferences
5. Follow the **Mizan** principle (balance) — don't over-flag, don't under-flag

## Deliverable

Create a file: `venus/tasks/001-code-review-prompt.txt`

The prompt should be ready to use as a system message for an LLM. Max 500 words.

## Acceptance Criteria

- [ ] Prompt covers: bugs, security, logic errors, performance
- [ ] Severity levels defined (critical, high, medium, low)
- [ ] Concise — under 500 words
- [ ] No model-specific instructions (must work with any LLM)
- [ ] Follows Mizan: balanced, not over-zealous
