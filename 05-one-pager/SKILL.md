# Skill 05 — One-pager brief

**Domain**: Strategy  
**Use when**: Creating a concise stakeholder brief for a new initiative — for alignment meetings, pre-reads, or sales enablement.  
**Time saved**: ~1–2 hours per brief

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}}.

Write a one-pager brief for the following initiative. This will be used as a {{purpose}}.

Initiative: {{initiative_name}}
Audience: {{audience}}
Problem: {{problem}}
Solution: {{solution}}
Key benefits: {{benefits}}
Timeline: {{timeline}}
Ask or next step: {{ask}}
Additional context: {{context}}

Write a crisp one-pager with these sections. Keep each section tight — this must fit one page.

## {{initiative_name}}

**The problem**
2–3 sentences. Make the pain real and quantifiable where possible.

**Our solution**
2–3 sentences. What it is, how it works at a high level, what makes it different.

**Who it's for**
One sentence per persona. Focus on their job to be done.

**Key outcomes**
3–4 bullet points. Business and customer outcomes, not features. Use numbers where possible.

**Timeline**
Simple milestone table or 3–4 bullet timeline.

**What we need**
The specific ask — decision, resource, approval, or awareness.

Tone should match {{audience}}. For exec audiences: outcome-first, no jargon, high confidence. For cross-functional partners: collaborative, transparent about trade-offs. For sales/CS: customer benefit-forward, avoids internal terminology.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{purpose}}` | How it will be used | Pre-read for a leadership alignment meeting / sales enablement brief / partner pitch |
| `{{initiative_name}}` | Name of the initiative | AI Scheduling Assistant |
| `{{audience}}` | Who will read it | VP Sales and Customer Success leadership |
| `{{problem}}` | Core problem | Managers spend avg. 4 hrs/week on shift scheduling; errors cost customers $X in overtime |
| `{{solution}}` | What you're building | AI assistant that auto-generates compliant schedules from availability and labor rules |
| `{{benefits}}` | Key outcomes | 60% reduction in scheduling time, 90% reduction in scheduling errors |
| `{{timeline}}` | Key dates | Beta: Q2, GA: Q3 |
| `{{ask}}` | What you need | Approval to include in Q3 launch communications and priority access for 5 pilot customers |
| `{{context}}` | Anything else useful | Builds on existing Time & Labor module, no new data integrations needed |

---

## Composability

Pipe the output of **Skill 04 (business case)** → this skill to create a stakeholder-friendly summary of a larger business case document.
