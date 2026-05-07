# Skill 07 — JIRA grooming

**Domain**: Execution  
**Use when**: Enriching an existing JIRA story with detailed acceptance criteria, edge cases, and grooming-ready detail before a sprint planning session.  
**Time saved**: ~20–40 min per story

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} grooming a JIRA story for sprint planning.

Story title: {{story_title}}
Story description / current content: {{story_content}}
Technical context: {{tech_context}}
Persona: {{persona}}
Definition of done at our team: {{dod}}

Improve and enrich this story so it is ready for sprint planning. Output:

## Improved user story

**As a** [persona]  
**I want to** [action]  
**So that** [outcome]

## Description
2–3 sentences of context for an engineer reading this cold. Include why this matters and what "good" looks like.

## Acceptance criteria
Write in Given/When/Then format. Cover:
- [ ] Happy path (at least 2)
- [ ] Validation and input errors
- [ ] Permission / role edge cases
- [ ] Empty states and loading states
- [ ] Failure / error states
- [ ] Analytics events to fire

## Edge cases to consider
Bullet list of scenarios the team should explicitly decide on before starting work. Flag which ones are in scope vs. need PM decision.

## Out of scope
Explicitly list what this story does NOT cover to prevent scope creep.

## Open questions
Any unresolved questions that need answers before work starts. Include a suggested owner for each.

## Definition of done checklist
- [ ] Acceptance criteria met
- [ ] Unit tests written
- [ ] Analytics events verified in staging
- [ ] Accessibility reviewed
- [ ] PM sign-off on staging demo
- [ ] [Add team-specific items from {{dod}}]

## Story point recommendation
Suggested estimate: [1 / 2 / 3 / 5 / 8]
Rationale: [1–2 sentences on complexity drivers]
Split recommendation: [Yes/No — if Yes, suggest how to split]
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{story_title}}` | JIRA story title | Employee can request PTO via AI chat interface |
| `{{story_content}}` | Current story text | As an employee, I want to request PTO through the AI assistant so I don't have to navigate the time-off module |
| `{{tech_context}}` | Relevant systems | Calls Time & Attendance API. Azure OpenAI for intent parsing. PTO balance from HR core. |
| `{{persona}}` | Primary user | Full-time employee, non-technical, uses mobile app primarily |
| `{{dod}}` | Your team's DoD | Unit tests, staging demo to PM, accessibility check, feature flag off by default |

---

## Tips

- Run this on output from **Skill 06 (JIRA epic)** to enrich individual stories before grooming sessions
- Add `{{past_bugs}}` with a short description of recent related bugs to prompt the model to generate regression-aware acceptance criteria
- Paste into JIRA description field directly — the markdown renders natively in most JIRA configurations
