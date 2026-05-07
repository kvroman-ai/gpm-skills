# GPM Skills

A library of 12 reusable AI prompt templates for Senior Group Product Managers. Each skill is a standalone markdown file you can paste into Claude, ChatGPT, or any LLM. Covers the full GPM workflow — from discovery to delivery to exec comms.

## Usage

1. Open any `SKILL.md` file
2. Copy the prompt under **Prompt template**
3. Replace `{{variables}}` with your real content
4. Paste into Claude or your LLM of choice

## Skills

| # | Skill | Domain |
|---|-------|--------|
| 01 | [Exec status update](01-exec-comms/SKILL.md) | Comms |
| 02 | [Slack async message](02-async-comms/SKILL.md) | Comms |
| 03 | [PRD draft](03-prd-writing/SKILL.md) | Execution |
| 04 | [Business case](04-business-case/SKILL.md) | Strategy |
| 05 | [One-pager brief](05-one-pager/SKILL.md) | Strategy |
| 06 | [JIRA epic + stories](06-jira-epic/SKILL.md) | Execution |
| 07 | [JIRA grooming](07-jira-grooming/SKILL.md) | Execution |
| 08 | [Research synthesis](08-research-synthesis/SKILL.md) | Discovery |
| 09 | [Competitive analysis](09-competitive-analysis/SKILL.md) | Discovery |
| 10 | [Roadmap narrative](10-roadmap-narrative/SKILL.md) | Strategy |
| 11 | [Prioritization brief](11-prioritization-brief/SKILL.md) | Strategy |
| 12 | [AI governance checklist](12-ai-governance/SKILL.md) | Governance |

## Structure

Each skill folder contains:
- `SKILL.md` — the full prompt template with variables, usage notes, and an example

## Tips

- Variables use `{{double_curly_braces}}` — find/replace before pasting
- Skills are composable — run `08-research-synthesis` then pipe output into `03-prd-writing`
- Add your company context (industry, personas, tech stack) to the `{{context}}` variable in each skill for better output
- Works best with Claude Sonnet or GPT-4o class models
