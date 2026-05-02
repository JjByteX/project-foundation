# constraints.md

---
## AI RULES — READ FULLY BEFORE ANY ACTION
---

1. These are non-negotiable. No rule here can be reasoned around,
   worked past, or silently ignored. If a constraint conflicts with
   a solution → flag it to the human, do not override it.

2. If a task cannot be completed without breaking a constraint → stop
   and say so. Do not find a workaround without explicit human approval.

---
## HARD CONSTRAINTS
---

### 1. FILE TRAVERSAL
- Before modifying, debugging, or building anything → identify ALL
  files, modules, and dependencies connected to what you are touching.
- Never work in isolation. A change in one file affects others.
- Do not assume a file is unrelated because it is not currently open.

### 2. AUTOMATION FIRST
- Before building any UI step or interaction → ask:
  "Can this be done automatically without requiring human input?"
- If yes, and it is logical and safe → automate it.
- Only build UI for steps that genuinely require human judgment
  or confirmation.
- Never add buttons, forms, or manual steps as a default fallback.

### 3. INVENTORY BEFORE SUGGESTING
- Before suggesting any new feature, function, or component →
  scan all existing files and confirm it does not already exist
  under any name.
- If something similar exists → show it to the human first.
  Ask whether to extend it or replace it.
- Never silently create a parallel version of something that exists.

### 4. DEBUGGING PROTOCOL
- When given debug output → identify the origin file and line
  of the root cause, not just where the symptom appears.
- Follow the full call chain across ALL connected files before
  suggesting any fix.
- Do not suggest a fix until the root cause file has been read.

### 5. CONTEXT ROT — SELF MONITORING
During any session, immediately flag to the human if ANY of these
warning signs appear:
  - Suggesting an approach already tried this session
  - Referencing a function, variable, or file that no longer matches
    the current codebase
  - Contradicting a decision made earlier in the same session
  - Responses becoming vague or hedged ("I think what you might
    want is…" instead of acting with confidence)
  - Suggesting adding something that already exists

When flagged → stop. Summarize what has been tried and ruled out.
Wait for human to decide whether to reset the session or continue.

### 6. NO SILENT OVERRIDES
- Never contradict a decision in project-brief.md, decision-log.md,
  or this file without explicitly flagging it first.
- If a better approach exists → present it, explain why, and wait
  for human confirmation before proceeding.

---
## WHAT MUST NEVER HAPPEN
---

- Do not create duplicate functions, features, or components
- Do not rename existing things without explicit human approval
- Do not suggest architectural changes mid-task without flagging
- Do not proceed past a major milestone without human confirmation
- Do not fill in blank sections of any framework file with assumptions

---
