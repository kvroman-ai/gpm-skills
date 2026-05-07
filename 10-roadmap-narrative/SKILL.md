# Skill 10 — Roadmap narrative

**Domain**: Strategy  
**Use when**: Writing the narrative behind a roadmap — explaining the "why" behind sequencing decisions for executives, customers, or the team.  
**Time saved**: ~1–2 hours per narrative

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} responsible for {{portfolio}}.

Write a roadmap narrative for {{audience}} covering {{time_horizon}}.

Strategic context: {{strategic_context}}
Key customer problems to solve: {{customer_problems}}
Business objectives: {{business_objectives}}
Constraints: {{constraints}}

Now / Next / Later initiatives:

NOW (current quarter):
{{now_initiatives}}

NEXT (following 1–2 quarters):
{{next_initiatives}}

LATER (6–12 months out):
{{later_initiatives}}

Write a roadmap narrative with the following structure:

## Where we're headed
2–3 sentences: the vision for this portfolio in {{time_horizon}}. What does success look like for customers and the business?

## Why this sequence
The core rationale for the Now / Next / Later ordering. This is the most important section — explain the logic, not just the list. Cover:
- What foundation we're building NOW and why it unlocks NEXT
- What customer problems are most urgent and why
- What we're intentionally deferring to LATER and why that's the right call
- Key constraints shaping sequencing (resources, dependencies, market timing)

## Now — {{current_quarter}}
For each initiative:
- **[Initiative name]**: One sentence on what it is and the outcome it drives. Why now.

## Next — {{next_period}}
For each initiative:
- **[Initiative name]**: One sentence on what it is. What it depends on from NOW. Why this order.

## Later — {{later_period}}
For each initiative:
- **[Initiative name]**: One sentence. Why it's later and not sooner — be honest about the trade-off.

## What's not on the roadmap (and why)
2–3 things that were considered and deprioritized. Showing this builds trust with stakeholders who will ask about them.

## Key assumptions and risks
What would cause this roadmap to change? List 3–5 assumptions we're making and the signal we'd watch for.

Write for {{audience}}. For executives: outcome-first, strategic, avoids implementation detail. For engineering teams: transparent about trade-offs and sequencing rationale. For customers: benefit-focused, avoids internal jargon.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{portfolio}}` | What you own | AI platform capabilities |
| `{{audience}}` | Who's reading | CPO and product leadership / Engineering team / Customer advisory board |
| `{{time_horizon}}` | How far out | 2026 H1 / 12 months / FY2026 |
| `{{strategic_context}}` | Company strategy | "Trusted AI experiences" platform pillar; enterprise upsell motion in HR and Finance |
| `{{customer_problems}}` | Top problems to solve | HR teams lack real-time workforce insights; employees can't self-serve answers to HR questions |
| `{{business_objectives}}` | OKRs or goals | Grow AI feature adoption to 40% of customers, reduce support tickets 20% |
| `{{constraints}}` | Hard limits | 2 eng teams, legal review required for any new data usage, no new vendor contracts in H1 |
| `{{now_initiatives}}` | Current work | AI benefits Q&A (GA), data retention framework, early access program |
| `{{next_initiatives}}` | Coming up | Workforce analytics natural language queries, AI scheduling assistant |
| `{{later_initiatives}}` | Future bets | Predictive turnover risk, compensation benchmarking AI, multi-modal document analysis |
