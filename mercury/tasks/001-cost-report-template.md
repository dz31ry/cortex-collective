# Task 001 — Cost Report Template

**Planet**: Mercury (Finance & Treasury)
**Type**: `docs`
**Difficulty**: Starter
**Time**: ~15 min

---

## Context

Mercury manages financial operations across the entire CORTEX OS ecosystem. Every AI agent consumes compute — tokens, API calls, processing time — and Mercury tracks it all.

### What Mercury Tracks

- **18 planet clusters** each have agents making LLM calls
- **Multiple LLM providers** (the system is model-agnostic — could be Claude, GPT, Gemini, Llama, or local models)
- **Per-agent costs** — some agents are cheap (simple classification), others are expensive (deep analysis, code generation)
- **Per-cluster budgets** — each planet has a monthly compute budget
- **Efficiency** — spending more doesn't always mean better output. The Mizan principle demands balance.

### Why This Matters

When you run 1,140+ agents across 18 clusters serving multiple ventures, cost visibility is survival. Without clear reporting:
- One cluster could burn through its budget unnoticed
- An inefficient agent could waste thousands in compute
- You can't optimize what you can't measure

### The Mizan Principle (Balance)

Mizan means "the balance." For cost reporting, this means:
- **Enough detail to act on** — don't hide important numbers behind summaries
- **Not so much detail it's unreadable** — a report should be scannable in 30 seconds
- **Efficiency matters** — raw cost alone is meaningless without quality context
- **Trends matter more than snapshots** — is spending going up, down, or stable?

## Task

Design a cost report template (markdown) that shows:

1. **Per-cluster breakdown** — how much each planet spent this period
2. **Per-model breakdown** — cost by LLM provider (remember: model-agnostic = multiple providers)
3. **Trend indicators** — up/down/stable compared to previous period
4. **Budget alerts** — which clusters are approaching their limits
5. **Efficiency score** — output quality vs. cost (the Mizan balance)

### Design Guidance

- Use markdown tables for structured data
- Use emoji or text indicators for trends (e.g. `↑` `↓` `→` or `UP` `DOWN` `STABLE`)
- Include a **summary section** at the top (the 30-second scan)
- Include a **details section** below (for deep dives)
- Make it useful for both humans AND agents (Mercury agents will parse this too)

### Example Data (Use Placeholder Numbers)

Some example clusters and their costs to give you a sense of scale:
- Mercury (Finance): $45.20/period — mostly simple ledger queries
- Venus (Dev): $312.80/period — heavy code generation and review
- Jupiter (Security): $189.50/period — continuous threat monitoring
- Saturn (Data): $256.30/period — data pipeline processing
- Total ecosystem: ~$2,100/period across all 18 clusters

## Deliverable

Create a file: `mercury/tasks/001-cost-report-template.md`

A markdown template with placeholder data. Should be clean, scannable, and useful for both humans and agents.

## Acceptance Criteria

- [ ] All 5 sections present (cluster breakdown, model breakdown, trends, budget alerts, efficiency)
- [ ] Summary section at top — scannable in 30 seconds
- [ ] Uses placeholder data (not real numbers)
- [ ] Clean markdown formatting (tables, headers, indicators)
- [ ] Covers all 18 clusters (can group smaller ones)
- [ ] Model-agnostic — shows multiple LLM providers
- [ ] Follows Mizan: balance between detail and clarity
