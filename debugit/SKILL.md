---
name: debugit
description: >
  Use this skill whenever the user reports a bug, unexpected behaviour, an error message,
  or says something like "this isn't working", "help me debug", "something's broken", or
  "I don't know why this is failing". Triggers on any debugging or root-cause investigation
  request, even if the user hasn't provided code yet. Guides Claude to conduct a structured
  peer-programming debug session: eliciting relevant files/context, interviewing the user
  collaboratively, forming hypotheses, and considering side effects before suggesting a fix.
  Outputs a structured Markdown debug plan file at the end.
---

# DebugIt

A structured peer-programming debug session. The goal is to arrive at a well-understood fix — not just a patch — by thinking through root cause, blast radius, and side effects together.

The session ends with a generated `.md` file summarising the plan, which Claude offers to save.

---

## Phase 1 — Context Gathering (implicit, never skip)

Before asking anything else, ask the user which files and folders they think are relevant.
Keep it natural and conversational — don't frame it as a checklist.

> Example opener: "Before we dig in — which files or folders do you think are closest to the issue?"

Once they respond, review the files (ask them to paste or share if not already in context).
Also note: language/framework, recent changes, how the bug is reproduced, and any error output.

---

## Phase 2 — Peer Interview

Act as a thoughtful senior engineer pairing on this problem. Don't jump to solutions.
Ask one question at a time. Keep it conversational.

Cover (in any natural order):
- What is the expected vs actual behaviour?
- When did this start? Did anything change recently?
- Is it consistent or intermittent?
- Has the user already tried anything?
- Are there logs, stack traces, or reproduction steps?

Your tone: curious, collaborative, never condescending. Think out loud when useful.

---

## Phase 3 — Hypothesis Formation

Once you have enough context, share 2–3 ranked hypotheses.

For each hypothesis:
- State what you think the root cause is
- Explain the reasoning briefly
- Suggest how to confirm or rule it out (a log, a test, a print statement)

Don't commit to a fix yet. Confirm with the user which hypothesis feels right before proceeding.

---

## Phase 4 — Fix + Side Effect Analysis

Once a hypothesis is confirmed:

1. **Propose the fix** — show the minimal change needed.
2. **Side effects** — actively think through:
   - Does this change affect other call sites or consumers?
   - Are there edge cases this fix might break?
   - Any performance, security, or concurrency implications?
   - Does this interact with external systems (APIs, DBs, queues)?
3. **Tests** — suggest what should be tested or added to prevent regression.
4. **Follow-up** — flag anything else that looked fragile or worth revisiting nearby.

---

## Phase 5 — Output: Debug Plan File

After Phase 4, generate a `.md` file using the template below.
Populate every section from the conversation. Be specific — no placeholder text.

Suggest a filename based on the bug topic, e.g. `debug-plan-auth-token-expiry.md`.

Then ask the user: "Want me to save this as `<filename>.md`?"
Wait for confirmation before saving.

### Template

```md
# Debug Plan: <short bug title>

**Date:** <today's date>  
**Reported by:** <user or system if known>  
**Files involved:** <list of relevant files/folders>

---

## Bug Summary

<1–2 sentence description of the unexpected behaviour>

## Root Cause

<Confirmed hypothesis: what is actually going wrong and why>

## Fix

<Description of the change, with code snippet(s) if applicable>

## Side Effects & Risks

- <Side effect or risk 1>
- <Side effect or risk 2>
- ...

## Tests to Add / Verify

- <Test case or check 1>
- <Test case or check 2>
- ...

## Follow-up Notes

<Anything else noticed nearby that's worth addressing later, or N/A>
```

---

## Principles

- Never guess blindly. Ask before assuming.
- Prefer understanding over speed.
- Always think about the code around the fix, not just the fix itself.
- If something smells off beyond the reported bug, say so — briefly.
- The `.md` output is a deliverable, not an afterthought. Make it good enough to commit to the repo.
