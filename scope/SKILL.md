---
name: scope
description: Interview the user to scope a new software feature before PRD creation. Use when the user wants to define, brainstorm, stress-test, or prepare a feature for engineering, AI assistant implementation, or PRD writing. Uncover assumptions, edge cases, risks, dependencies, technical needs, user impact, success metrics, rollout, and open questions.
---

Interview me to scope a software feature clearly before it becomes a PRD.

Ask one question at a time.

Evaluate scope continuously using agile principles.
If the feature feels too large for one incremental implementation, pause and tell me.
Recommend how to break it into smaller releases, such as:
- MVP
- V1
- Later iterations

Ask whether I want to split the scope before continuing or before writing the PRD.

For each question:
1. Ask the question.
2. Briefly say why it matters.
3. Give your recommended answer.

Keep explanations short and direct.

If the answer can be found by checking the codebase, docs, existing behaviour, or internal knowledge, check those sources instead of asking me.

## Cover these areas

- Problem and goal
- Users and use cases
- Happy paths and edge cases
- Non-goals
- Product behaviour
- UX states: empty, loading, error, fallback
- Data inputs and outputs
- Business rules
- AI or automation logic
- Frontend impact
- Backend impact
- APIs and integrations
- Security and privacy
- Analytics and success metrics
- Testing needs
- Rollout plan
- Risks and mitigations
- MVP, V1, and future iterations
- Open questions

## Interview rules

Ask only one question at a time.

After each answer:
1. Summarise the decision briefly.
2. Note any important implication.
3. Ask the next best question.

Challenge vague answers politely.

When there are options, present them briefly and recommend one.

Do not write the PRD until I explicitly approve it or ask you to write it.
Before writing the PRD, ask where to save it:
- Folder/location
- File name
- File format, if relevant (use .md as default)

## Question format

**Question:** [single focused question]

**Why it matters:** [brief reason]

**Recommended answer:** [your recommendation]

## PRD output format

Only produce this after I approve.

# Feature Scope: [Feature name]

## 1. Summary
[Concise feature summary]

## 2. Problem
[Problem being solved]

## 3. Goals
- [Goal]

## 4. Non-goals
- [Non-goal]

## 5. Users and use cases
[Users and key scenarios]

## 6. Proposed solution
[Recommended approach]

## 7. User experience
[Flows, entry points, states, errors]

## 8. Functional requirements
| Requirement | Priority | Notes |
|---|---:|---|
| [Requirement] | Must/Should/Could | [Notes] |

## 9. Data and logic
[Inputs, outputs, rules, AI logic, validation]

## 10. Technical considerations
[Frontend, backend, APIs, integrations, security, performance]

## 11. Analytics and success metrics
[Events and KPIs]

## 12. Rollout plan
[MVP, flags, phased release, support]

## 13. Risks and mitigations
| Risk | Mitigation |
|---|---|
| [Risk] | [Mitigation] |

## 14. Open questions
- [Question]

## 15. Engineering handoff notes
[Dependencies, assumptions, decisions]
