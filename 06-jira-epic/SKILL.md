# Skill 06 — JIRA epic + story breakdown

**Domain**: Execution  
**Use when**: Turning a feature idea or PRD into a structured JIRA epic with child stories, ready for sprint planning.  
**Time saved**: ~1–3 hours per epic

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} working on {{product_area}}.

Break down the following feature into a JIRA epic with user stories.

Feature / initiative: {{feature_name}}
Description: {{feature_description}}
Personas: {{personas}}
Technical context: {{tech_context}}
Out of scope: {{out_of_scope}}
Target sprint or quarter: {{timeline}}

Output the following:

## Epic

**Epic name**: [Action-oriented name, under 60 chars]
**Epic description**: 2–3 sentences — the "why" and "what" for engineers and designers reading this cold.
**Acceptance criteria for the epic**:
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3 (add as many as needed)

---

## User stories

For each story, use this format:

### Story [N]: [Short title]
**As a** [persona]  
**I want to** [action]  
**So that** [outcome / value]  

**Acceptance criteria**:
- [ ] Given [context], when [action], then [result]
- [ ] (add 3–5 ACs per story)

**Story points estimate**: [1 / 2 / 3 / 5 / 8 — with brief rationale]
**Dependencies**: [Other stories or systems this depends on]
**Notes**: [Edge cases, open questions, design considerations]

---

Generate 6–10 stories that cover the full scope of the epic. Include:
- Core happy path stories
- Error and edge case stories
- At least one analytics / instrumentation story
- Any infrastructure or migration stories if applicable

Order stories by recommended implementation sequence.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{product_area}}` | What you own | AI assistant — HR workflows |
| `{{feature_name}}` | Feature name | AI-powered PTO request handler |
| `{{feature_description}}` | What it does | Employees ask for PTO in natural language; AI checks balance, policy, and team calendar, then routes for approval or auto-approves within policy |
| `{{personas}}` | Who uses it | Employee (requester), Manager (approver), HR admin (policy config) |
| `{{tech_context}}` | Relevant tech | Built on existing Time & Attendance APIs. Uses Azure OpenAI. PII must stay on-prem. |
| `{{out_of_scope}}` | Explicit non-goals | Multi-country leave types, FMLA handling, mobile push notifications |
| `{{timeline}}` | Target | Q2 sprint 3–5 |

---

## Tips

- Feed the output directly into **Skill 07 (JIRA grooming)** to enrich acceptance criteria on complex stories
- Add a `{{team_velocity}}` variable to prompt the model to flag which stories are too large and should be split
- For platform/infrastructure epics, add `{{system_diagram}}` with a text description of your architecture to get more accurate dependency mapping
