# Skill 02 — Slack async message

**Domain**: Communications  
**Use when**: Drafting Slack messages for blockers, alignment pings, risk flags, standup updates, or launch announcements.  
**Time saved**: ~10–20 min per message

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}}.

Draft a Slack message for the following situation.

Message type: {{message_type}}
Tone: {{tone}}
Channel / audience: {{channel_and_audience}}

Situation:
{{situation}}

Write a Slack message that:
- Gets to the point in the first line — people skim Slack
- Sounds like a real person, not a corporate memo
- Uses minimal formatting: 1–2 emoji max, short bullets only if genuinely needed, no headers
- Ends with a clear next step, question, or call to action
- Is appropriately brief for async reading — under 150 words unless the situation genuinely demands more
- Matches a {{tone}} tone throughout

Output only the Slack message. No preamble, no explanation, no quotes around it.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{message_type}}` | Type of message | Blocker / escalation, Risk flag, Standup update, Alignment ping, Decision needed, Launch announcement |
| `{{tone}}` | Desired tone | Calm and professional, Urgent but not alarming, Direct and concise, Collaborative, Celebratory |
| `{{channel_and_audience}}` | Where it's going | #ai-platform-team — engineering leads and design, not exec-facing |
| `{{situation}}` | What happened | Engineering is 2 sprints behind because of an undiscovered dependency on the data platform team |

---

## Example input

```
{{company}}: Paylocity
{{message_type}}: Blocker / escalation
{{tone}}: Calm but urgent
{{channel_and_audience}}: #ai-platform-leads — engineering leads, design, no execs in this channel

{{situation}}: We're blocked on the AI assistant rollout because the data platform team's API isn't ready. It was supposed to be done last Friday. We need to either get a firm commit from data platform this week or decide to mock the integration for the demo and do a real integration post-launch. I need everyone aligned by EOD tomorrow.
```

## Example output

```
Hey team — flagging a blocker on the AI assistant rollout 🚨

Data platform API was due last Friday and isn't ready yet. This is now on the critical path for our launch timeline.

Two options I see:
• Get a firm delivery commit from data platform this week (I can escalate if helpful)
• Mock the integration for the demo, ship real integration post-launch

I need us aligned by EOD tomorrow so we can adjust the plan. Can everyone weigh in here or jump on a 20-min call tomorrow AM?
```
