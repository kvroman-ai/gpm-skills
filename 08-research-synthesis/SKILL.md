# Skill 08 — Research synthesis

**Domain**: Discovery  
**Use when**: Turning raw customer interview notes, survey results, or support ticket data into structured insights and themes.  
**Time saved**: ~2–4 hours per synthesis

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} synthesizing customer research.

Research type: {{research_type}}
Research goal / question: {{research_question}}
Number of sources: {{source_count}}
Personas represented: {{personas}}

Raw research data:
{{raw_data}}

Synthesize this research into a structured insights document. Output:

## Research summary
3–4 sentences: what you set out to learn, how many sources, what emerged overall.

## Top themes
For each theme (aim for 4–6):

### Theme [N]: [Descriptive theme name]
**Frequency**: Mentioned by X of Y sources  
**Strength**: High / Medium / Low signal  
**Summary**: 2–3 sentences describing the theme.  
**Supporting evidence** (direct quotes or paraphrased data points):
- "[Quote or data point]" — [Persona / source type]
- "[Quote or data point]" — [Persona / source type]
**Implication for product**: What this means for what we should build or prioritize.

## Key tensions or contradictions
Things customers said that pull in opposite directions. Useful for identifying trade-offs.

## Jobs to be done
What customers are actually trying to accomplish (using JTBD format):
- When [situation], I want to [motivation], so I can [outcome]

## Surprising findings
Things that contradicted assumptions or were unexpected. Flag these explicitly.

## Confidence assessment
| Theme | Confidence | Why |
|-------|------------|-----|
| Theme 1 | High | Consistent across all personas, quantitative backing |
| Theme 2 | Medium | Strong signal from 1 persona, weaker from others |

## Recommended next steps
3–5 specific actions — further research needed, features to explore, hypotheses to test.

Be rigorous about distinguishing evidence from inference. Label assumptions clearly.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{research_type}}` | Type of input | Customer interviews / Support ticket analysis / NPS survey verbatims / Sales call transcripts |
| `{{research_question}}` | What you were trying to learn | Why do HR admins avoid using the AI features we've shipped? |
| `{{source_count}}` | How many inputs | 12 customer interviews, 3 CSM interviews |
| `{{personas}}` | Who was represented | HR admin (8), Benefits manager (3), CHRO (1) |
| `{{raw_data}}` | Your notes | Paste interview notes, survey responses, support tickets |

---

## Composability

- Feed output into **Skill 03 (PRD draft)** — the themes map to the "Problem" section
- Feed output into **Skill 04 (business case)** — use themes as evidence in "The opportunity" section
- Feed output into **Skill 10 (roadmap narrative)** — use JTBD statements to justify roadmap priorities
