# Skill 04 — Business case

**Domain**: Strategy  
**Use when**: Building a business case for a new initiative, budget request, or investment decision.  
**Time saved**: ~3–5 hours per business case

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} making a business case for {{initiative_name}}.

Write a compelling business case document for this initiative.

Initiative: {{initiative_name}}
Problem / opportunity: {{opportunity}}
Proposed solution: {{solution}}
Target customer segment: {{segment}}
Estimated investment: {{investment}}
Key data points available: {{data_points}}
Strategic alignment: {{strategic_alignment}}
Alternatives considered: {{alternatives}}

Write a business case with the following sections:

## Executive summary
3–4 sentences: the opportunity, the proposed investment, the expected return, and the recommendation.

## The opportunity
- Market or customer problem being solved
- Size of the opportunity (TAM/SAM or number of customers affected)
- Why now — urgency, market timing, or competitive pressure
- Cost of inaction

## Proposed solution
- What we're building and for whom
- How it works (high level — this is not a PRD)
- Key differentiators vs. status quo or alternatives

## Investment required
- Engineering / design / PM effort (rough)
- Licensing, infrastructure, or vendor costs
- Timeline to first value / full rollout

## Expected return
- Revenue impact (new ARR, expansion, retention)
- Cost savings or efficiency gains
- Customer metrics (NPS, adoption, ticket deflection)
- How you're estimating these — be explicit about assumptions

## Risks
- Top 3 risks with likelihood and mitigation
- What would cause this to fail

## Alternatives considered
For each alternative: what it is, why we're not doing it.

## Recommendation
Clear ask: approve / fund / resource. What you need and by when.

Be honest about assumptions. Flag what's known vs. estimated. Executives trust candid analysis more than polished optimism.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{initiative_name}}` | What you're proposing | AI-powered workforce analytics dashboard |
| `{{opportunity}}` | The problem or market gap | 60% of mid-market HR teams lack real-time workforce insights, leading to reactive headcount decisions |
| `{{solution}}` | What you're building | LLM-powered natural language query interface on top of existing workforce data |
| `{{segment}}` | Who benefits | Mid-market customers (500–2000 employees), Finance and HR leaders |
| `{{investment}}` | Rough cost | 4 engineers × 2 quarters + $200K infra |
| `{{data_points}}` | Evidence you have | Customer interviews (12), support ticket analysis, competitive teardown |
| `{{strategic_alignment}}` | How it fits strategy | Supports "trusted AI experiences" platform pillar and enterprise upsell motion |
| `{{alternatives}}` | What else was considered | Buy vs. build, partner with BI vendor, enhance existing reports |

---

## Tips

- Run this after **Skill 08 (research synthesis)** to populate `{{data_points}}` with real customer evidence
- Use the output as the foundation for exec presentations — the sections map directly to slide structure
- For the "Expected return" section, prompt the model with your specific ARR per customer and churn assumptions for tighter numbers
