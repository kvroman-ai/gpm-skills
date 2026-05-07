# Skill 12 — AI governance checklist

**Domain**: Governance  
**Use when**: Running a risk and compliance review on an AI feature before launch — covers data usage, privacy, explainability, human oversight, and regulatory considerations.  
**Time saved**: ~1–2 hours per feature review

---

## Prompt template

```
You are a Senior Group Product Manager at {{company}} conducting an AI governance review for {{feature_name}}.

Feature description: {{feature_description}}
Data used: {{data_inputs}}
AI/ML components: {{ai_components}}
User personas affected: {{personas}}
Regulatory environment: {{regulatory_context}}
Existing guardrails: {{existing_guardrails}}

Produce a comprehensive AI governance review with the following sections:

## Feature summary
2–3 sentences on what the feature does, who it affects, and what AI capabilities it uses.

## Data governance

### Data inputs
For each data input:
- Data type and sensitivity classification (public / internal / confidential / restricted / PII / PHI)
- Source and ownership
- Retention policy (how long is it stored, where)
- Access controls (who can access this data)
- Whether it leaves the org boundary (e.g., sent to third-party LLM APIs)

### Data outputs
- What data or insights does the AI produce?
- Who sees the output?
- Is output stored? For how long?
- Can output be used to re-identify individuals?

## Model and AI risk

### Model transparency
- [ ] Can we explain why the model produced a given output? (Explainability)
- [ ] Is there a human-in-the-loop for high-stakes decisions?
- [ ] Are model limitations clearly communicated to users?
- [ ] Is there a feedback mechanism for incorrect outputs?

### Bias and fairness
- [ ] Have we evaluated the model for demographic or protected-class bias?
- [ ] Are there populations that may be systematically disadvantaged by this feature?
- [ ] What's our monitoring plan for detecting bias post-launch?

### Reliability and failure modes
- [ ] What happens when the model is wrong or uncertain?
- [ ] Is there a graceful fallback to a non-AI path?
- [ ] What's the worst-case outcome of a model error for a user?

## Privacy and compliance

### Regulatory requirements
For each applicable regulation (GDPR, CCPA, HIPAA, SOC 2, state AI laws, etc.):
- Requirement: [What the regulation requires]
- Current status: [Compliant / At risk / Unknown]
- Action needed: [What needs to happen before launch]

### Consent and transparency
- [ ] Do users know they're interacting with AI?
- [ ] Is there a clear disclosure of what data is used?
- [ ] Can users opt out of AI features while retaining core functionality?
- [ ] Is there a process for users to request deletion of AI-derived data?

## Vendor and third-party risk
For each AI vendor or third-party model:
- Vendor name and model used
- Data processing agreement (DPA) in place: Yes / No / In progress
- Data residency: Where is data processed and stored?
- Subprocessors: Does the vendor share data with others?
- Right to train on our data: Explicitly prohibited? (flag if unclear)
- Security certifications: SOC 2, ISO 27001, etc.

## Launch readiness checklist
- [ ] Legal review completed
- [ ] Security review completed
- [ ] Privacy impact assessment (PIA) completed
- [ ] DPAs signed with all AI vendors
- [ ] User disclosure / consent language approved
- [ ] Human escalation path documented
- [ ] Model performance baselines established
- [ ] Monitoring and alerting in place
- [ ] Incident response plan updated to cover AI failure scenarios
- [ ] Training for CS and support on AI limitations

## Risk summary

| Risk | Severity | Likelihood | Owner | Mitigation |
|------|----------|------------|-------|------------|
| [Risk] | High/Med/Low | High/Med/Low | [Name] | [Action] |

## Recommendation
Go / Go with conditions / No go — with clear rationale and, if conditional, the specific items that must be resolved before launch.
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{company}}` | Your company | Paylocity |
| `{{feature_name}}` | Feature being reviewed | AI benefits Q&A assistant |
| `{{feature_description}}` | What it does | Employees ask natural language questions about their benefits; AI answers using plan documents |
| `{{data_inputs}}` | Data the AI uses | Employee benefits enrollment data, plan documents (PDFs), employee ID |
| `{{ai_components}}` | Models and systems | Azure OpenAI GPT-4o for response generation, internal RAG pipeline on plan docs |
| `{{personas}}` | Affected users | All employees, HR admins (policy config), benefits brokers (document upload) |
| `{{regulatory_context}}` | Applicable regulations | ERISA, CCPA, SOC 2 Type II, state AI transparency laws |
| `{{existing_guardrails}}` | What's already in place | PII scrubbing before LLM calls, no data sent to OpenAI training, on-prem vector store |

---

## Tips

- Run this before every AI feature launch — share output with Legal and Security as the formal review artifact
- The "Vendor and third-party risk" section doubles as a procurement checklist for new AI vendor evaluations
- Pipe into **Skill 01 (exec status update)** to surface governance blockers in weekly status
- Revisit quarterly as regulations evolve — AI governance is not a one-time exercise
