# Skill 03 — PRD draft

**Domain**: Execution  
**Use when**: Writing a Product Requirements Document from a problem statement, customer insight, or rough feature idea.  
**Time saved**: ~2–4 hours per PRD

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} working on {{product_area}}.

Write a comprehensive PRD for the following initiative.

Initiative name: {{initiative_name}}
Problem statement: {{problem_statement}}
Target persona(s): {{personas}}
Key constraints: {{constraints}}
Success metrics: {{success_metrics}}
Additional context: {{context}}

Write a PRD with the following sections:

## Overview
One paragraph: what this is, why now, who it's for.

## Problem
- What pain are we solving? Use customer language where possible.
- What happens today without this solution?
- What's the cost of inaction (to customers and the business)?

## Goals & success metrics
- Primary metric (the one that matters most)
- Secondary metrics (2–3 supporting indicators)
- Non-goals (explicitly out of scope)

## Personas & use cases
For each persona: who they are, their current pain, their primary use case for this feature.

## Requirements
### Must have (P0)
### Should have (P1)
### Nice to have (P2)

## User experience
- Key user flows (narrative, not wireframes)
- Edge cases and error states to consider

## Technical considerations
- Known dependencies
- Data requirements
- Privacy / compliance / security flags
- Scalability considerations

## Open questions
- Unresolved decisions with owner and due date

## Launch & GTM considerations
- Rollout approach (GA, beta, feature flag, early access)
- Enablement needs (sales, CS, support)
- Key risks to launch

Use clear, direct language. Write requirements as outcomes where possible ("Users can X" not "The system shall Y"). Flag assumptions explicitly.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{product_area}}` | What you own | AI assistant capabilities for HR workflows |
| `{{initiative_name}}` | Feature or initiative name | AI-powered benefits recommendation engine |
| `{{problem_statement}}` | Core problem in 1–3 sentences | HR admins spend 3+ hours per open enrollment answering employee benefits questions that are already answered in plan documents |
| `{{personas}}` | Who this is for | HR admin (primary), Employee (secondary) |
| `{{constraints}}` | Hard limits | Must use existing LLM vendor contract, no PII in prompts, launch by Q3 |
| `{{success_metrics}}` | How you'll know it worked | 30% reduction in benefits-related HR tickets, 80%+ employee satisfaction with answers |
| `{{context}}` | Any extra context | Competitor launched similar feature in Jan. We have 2 engineers available. |

---

## Example input

```
{{company}}: Paylocity
{{product_area}}: AI platform — HR workflow automation
{{initiative_name}}: AI benefits Q&A assistant
{{problem_statement}}: During open enrollment, HR admins field hundreds of repetitive employee questions about plan options, deductibles, and eligibility. Most answers exist in plan documents but employees don't read them. This consumes significant HR time and delays employee decision-making.
{{personas}}: HR admin (primary), Employee self-service user (secondary)
{{constraints}}: Must not send PII to third-party LLMs. Must work within existing Azure OpenAI contract. Target Q3 GA.
{{success_metrics}}: 25% reduction in benefits tickets to HR during open enrollment. Employee self-service answer satisfaction > 75%.
{{context}}: Two similar features launched by competitors in H1. We have plan document ingestion infrastructure already built for another feature.
```
