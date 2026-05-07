# Skill 09 — Competitive analysis

**Domain**: Discovery  
**Use when**: Producing a structured competitive landscape summary for a feature area, product decision, or market positioning exercise.  
**Time saved**: ~2–3 hours per analysis

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} conducting a competitive analysis for {{feature_area}}.

Competitors to analyze: {{competitors}}
Our current capability: {{our_capability}}
Strategic question we're trying to answer: {{strategic_question}}
Raw competitive data / inputs: {{raw_data}}

Produce a structured competitive analysis with the following sections:

## Landscape overview
2–3 sentences on the competitive environment for this feature area. Who's leading, where's the market heading.

## Competitor profiles
For each competitor:

### [Competitor name]
**Positioning**: How they describe this capability  
**What they've built**: What the feature actually does (factual, not marketing)  
**Strengths**: What they do well  
**Weaknesses / gaps**: Where they fall short  
**Who they target**: Segment, persona, use case  
**Launch timeline**: When they shipped this, how it's evolved  
**Pricing / packaging**: If known  
**Key differentiator vs. us**: One sentence

## Capability comparison matrix
| Capability | Us | [Competitor 1] | [Competitor 2] | [Competitor 3] |
|------------|----|----------------|----------------|----------------|
| [Feature]  | ✓ / ✗ / ~ | | | |

Use: ✓ = fully supported, ~ = partial/limited, ✗ = not available, ? = unknown

## Where we lead
Honest assessment of our genuine advantages. Flag if advantages are durable vs. temporary.

## Where we lag
Gaps vs. the market. Flag which gaps are table stakes vs. differentiating.

## Strategic implications
- What does this mean for our roadmap?
- Where should we compete, and where should we differentiate?
- What's the risk of our current position?

## Recommended actions
3–5 specific, actionable recommendations based on this analysis.

## Confidence and gaps in data
What you know vs. what you're inferring. What additional research would sharpen this.

Be objective. Avoid cheerleading for our own product. Executives and engineers trust honest analysis.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{feature_area}}` | The capability being analyzed | AI-powered HR assistant / workforce analytics |
| `{{competitors}}` | Who to analyze | Workday, ADP, Rippling, Gusto, Lattice |
| `{{our_capability}}` | What we have today | Early access AI assistant, limited to PTO and benefits Q&A |
| `{{strategic_question}}` | What decision this informs | Should we accelerate our AI roadmap or focus on depth in existing features? |
| `{{raw_data}}` | Your research | Product teardowns, G2 reviews, press releases, sales battle cards, demo recordings |

---

## Tips

- Paste G2 or Capterra review excerpts into `{{raw_data}}` for customer-voice competitive intelligence
- Use this before **Skill 04 (business case)** to populate the "Why now" and "Market timing" sections
- Add `{{ideal_customer_profile}}` to filter competitive analysis through the lens of your target segment
