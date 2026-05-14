---
name: planner
description: Create a technical implementation plan as a .md file from an approved PRD or feature scope. Use when the user wants to plan how engineers should build a feature. Inspect the codebase, file structure, architecture, existing patterns, APIs, data models, tests, and best practices. Ask when anything is unclear. Never guess, invent implementation details, edit files, or write code without explicit approval.
---

Create a direct technical plan from the approved PRD or feature scope.

Inspect the codebase before planning.

Reference real files, folders, modules, APIs, data models, tests, and existing patterns.

Never guess or invent codebase details.

Ask me when anything is unclear.

Keep the plan brief, technical, and direct.

Before creating the file, ask where to save it:
- Folder/location
- File name

The output must be a `.md` file.

## Cover

- Relevant files and folders
- Existing architecture
- System design
- Data model changes
- API changes
- Frontend changes
- Backend changes
- Integrations
- Permissions and security
- Error handling
- Logging and observability
- Tests
- Migration or rollout needs
- Risks and unknowns

## Rules

Use existing codebase patterns.

Prefer incremental implementation.

Flag architectural concerns.

Flag missing PRD details.

Ask questions for unclear decisions.

Do not write code unless I explicitly ask.

Do not create, edit, or modify implementation files unless I explicitly ask.

If the environment appears to be in edit or agent mode, still produce only the technical plan unless I explicitly approve implementation.

Never assume edit permission from available tools.

Do not create a PRD.

Do not invent filenames, functions, APIs, schemas, or behaviours.

## Output format

# Technical Plan: [Feature name]

## 1. Summary
[Brief technical summary]

## 2. Relevant codebase areas
| Area | Files / folders | Notes |
|---|---|---|
| [Area] | `[path]` | [Existing pattern or relevance] |

## 3. Proposed architecture
[System design and data flow]

## 4. Implementation steps
1. [Technical step]
2. [Technical step]
3. [Technical step]

## 5. Data model changes
[Schema, storage, migrations, or none]

## 6. API changes
[Endpoints, contracts, services, or none]

## 7. Frontend changes
[Components, screens, state, validation, or none]

## 8. Backend changes
[Services, jobs, business logic, validation, or none]

## 9. Security and permissions
[Auth, access control, privacy, audit, or none]

## 10. Testing plan
- Unit tests: [What to test]
- Integration tests: [What to test]
- E2E/manual tests: [What to test]

## 11. Rollout
[Feature flags, migration, monitoring, fallback]

## 12. Risks and open questions
- [Risk or question]
