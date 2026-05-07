# Skill 01 — Exec status update

**Domain**: Communications  
**Use when**: Writing weekly or bi-weekly portfolio status updates for CPO, C-suite, or VP-level leadership.  
**Time saved**: ~30–45 min per update

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} responsible for {{portfolio_description}}.

Write an executive status update for {{audience}} covering the period {{date_range}}.

Overall portfolio status: {{status}} (On track / At risk / Blocked / Ahead of plan)

Raw notes and inputs:
{{raw_notes}}

Decisions or asks needed:
{{asks}}

Format the output with these sections:
- **Status**: One line with a status indicator (🟢 On track / 🟡 At risk / 🔴 Blocked)
- **Summary**: 2–3 sentences on what matters most this period — outcomes, not activities
- **Progress**: 4–6 bullet points, written as outcomes ("Launched X to Y customers" not "Worked on X")
- **Risks & blockers**: 2–3 bullets with owner and mitigation if known. Omit section if none.
- **Asks / decisions needed**: Specific, time-bound asks. Omit section if none.
- **Coming up**: 3–4 bullets on next period priorities

Tone: Confident, direct, outcome-focused. Written for {{audience}} — strip out implementation details, lead with business impact. No filler sentences.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company name | Paylocity |
| `{{portfolio_description}}` | What you own | AI platform capabilities across HR and payroll |
| `{{audience}}` | Who's reading | CPO and C-suite |
| `{{date_range}}` | Period covered | Week of May 5, 2026 |
| `{{status}}` | Overall RAG status | At risk |
| `{{raw_notes}}` | Your unfiltered notes | Bullet dump, meeting notes, Slack threads |
| `{{asks}}` | Decisions you need | Legal sign-off on data retention by Friday |

---

## Example input

```
{{company}}: Paylocity
{{portfolio_description}}: trusted AI experiences across HR, payroll, and workforce management
{{audience}}: CPO and VP Engineering
{{date_range}}: Week of May 5, 2026
{{status}}: At risk

{{raw_notes}}:
- AI assistant feature shipped to early access — 3 enterprise customers onboarded
- Blocked on legal review for data retention policy, been waiting 2 weeks
- Engineering flagged scalability risk in vector DB at 10k+ concurrent users
- Roadmap review with CPO scheduled for next week
- Customer NPS on AI assistant: 72 (above 65 target)
- Competitor launched similar feature last week — need to accelerate differentiation story

{{asks}}: Need legal sign-off on data retention policy by May 10. Need CPO decision on scope trade-off for Q2 milestone.
```

## Example output

```
**Status**: 🟡 At risk — legal dependency threatening Q2 milestone

**Summary**: AI assistant early access is live with strong initial signal (NPS 72 vs. 65 target). A two-week legal review delay on data retention policy is now the critical path risk for the Q2 milestone. Engineering has also flagged a scalability concern that needs architectural decision before broader rollout.

**Progress**:
- AI assistant shipped to early access; 3 enterprise customers onboarded with above-target NPS (72)
- Vector DB performance benchmarked at scale — identified ceiling at 10k concurrent users
- Competitive landscape update completed; differentiation brief in progress
- Q2 roadmap finalized pending CPO alignment session (scheduled May 12)

**Risks & blockers**:
- 🔴 Legal review on data retention policy — 2 weeks overdue, now on critical path. Ask: sign-off by May 10 or escalation path needed.
- 🟡 Vector DB scalability risk at 10k+ users — architectural options under review with Engineering. Decision needed before broad rollout.

**Asks / decisions needed**:
1. Legal: Data retention policy approval by May 10 — who can unblock?
2. CPO: Q2 scope trade-off decision at May 12 roadmap review

**Coming up**:
- CPO roadmap review — Q2 milestone alignment
- Onboard 5 additional early access customers
- Engineering architectural decision on vector DB
- Draft differentiation narrative vs. competitor launch
```
