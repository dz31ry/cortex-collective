# Task 001 — Cost Report Template

**Planet**: Mercury (Finance & Treasury)
**Type**: `docs`
**Difficulty**: Starter
**Time**: ~15 min

---

## Context

Mercury manages financial operations across the ecosystem. Every AI agent consumes compute — tokens, API calls, processing time. Mercury needs clear cost reporting.

## Task

Design a cost report template (markdown) that shows:

1. **Per-cluster breakdown** — how much each planet spent this period
2. **Per-model breakdown** — cost by LLM provider (model-agnostic, so multiple providers)
3. **Trend indicators** — up/down/stable compared to previous period
4. **Budget alerts** — which clusters are approaching their limits
5. **Efficiency score** — output quality vs. cost (the Mizan balance)

## Deliverable

Create a file: `mercury/tasks/001-cost-report-template.md`

A markdown template with placeholder data. Should be clean, scannable, and useful for both humans and agents.

## Acceptance Criteria

- [ ] All 5 sections present
- [ ] Uses placeholder data (not real numbers)
- [ ] Clean markdown formatting
- [ ] Scannable in under 30 seconds
- [ ] Follows Mizan: balance between detail and clarity
