# Skill 11 — Prioritization brief

**Domain**: Strategy  
**Use when**: Scoring and ranking a backlog of initiatives using a structured framework (RICE, impact/effort, or custom), and producing a defensible recommendation.  
**Time saved**: ~1–2 hours per prioritization session

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} prioritizing a backlog of initiatives for {{portfolio}}.

Prioritization framework: {{framework}}
Decision being made: {{decision}}
Stakeholders this will go to: {{stakeholders}}
Timeframe: {{timeframe}}
Constraints: {{constraints}}

Initiatives to evaluate:
{{initiatives}}

Scoring assumptions:
{{scoring_assumptions}}

Produce a prioritization brief with the following sections:

## Decision context
1–2 sentences: what decision we're making, why now, who will use this.

## Scoring methodology
Explain the framework being used and how each dimension is scored. Be explicit about assumptions so stakeholders can challenge them.

## Prioritization table

| Initiative | {{dimension_1}} | {{dimension_2}} | {{dimension_3}} | Score | Rank |
|------------|-----------------|-----------------|-----------------|-------|------|
| [Name]     | [Score]         | [Score]         | [Score]         | [Total] | [#] |

For RICE: columns are Reach, Impact, Confidence, Effort, RICE Score
For Impact/Effort: columns are Customer Impact, Business Impact, Effort, Score
For custom: define your own columns

## Initiative summaries
For each initiative in ranked order:

### [Rank]. [Initiative name] — Score: [X]
- **What it is**: One sentence
- **Why this score**: 2–3 sentences explaining the key drivers of the score and any important caveats
- **Key risk**: The main thing that could make this score wrong

## Recommendation
Top 3 initiatives to pursue in {{timeframe}}, with rationale. Be opinionated — don't just report the scores, make a recommendation.

## What we're not doing (and why)
Bottom 2–3 initiatives and the honest reason they didn't make the cut.

## Assumptions and sensitivities
What would change the ranking? List the top 3 assumptions that, if wrong, would shuffle the order.

Be honest about uncertainty. A prioritization framework is a thinking tool, not a truth machine.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{portfolio}}` | What you're prioritizing | AI platform H2 roadmap |
| `{{framework}}` | Scoring model | RICE / Impact-Effort / Weighted scoring / Custom |
| `{{decision}}` | What you're deciding | Which 3 initiatives get engineering resources in H2 2026 |
| `{{stakeholders}}` | Who sees this | CPO, VP Engineering, Head of Design |
| `{{timeframe}}` | Planning horizon | H2 2026 (2 engineering teams, 6 months) |
| `{{constraints}}` | Hard limits | Max 2 initiatives per team, no new vendor contracts, legal review adds 4 weeks to any data initiative |
| `{{initiatives}}` | What you're ranking | List each initiative with a short description |
| `{{scoring_assumptions}}` | Your calibration | Reach: # of customers impacted per quarter. Impact: 3=transformative, 2=significant, 1=incremental. Effort in eng-weeks. |
| `{{dimension_1/2/3}}` | Framework dimensions | Reach, Impact, Confidence (for RICE) |

---

## Composability

- Use output from **Skill 08 (research synthesis)** to calibrate Impact scores with real customer evidence
- Use output from **Skill 09 (competitive analysis)** to factor in strategic urgency vs. competitors
- Feed ranked output into **Skill 10 (roadmap narrative)** to explain the sequencing to stakeholders
