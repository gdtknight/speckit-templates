# AGENTS.md

This file defines the global rules for all agents (Codex, Copilot, Gemini) working in this repository.
These rules are mandatory and override any default behavior.

---

## Single Source of Truth (SSOT)

The following files and directories are the ONLY authoritative sources of truth.

Priority order (highest first):

1) AGENTS.md  
2) memory/constitution.md  
3) memory/context.md  
4) spec/*  
5) tasks/*  
6) README and source files  

If there is any conflict, always follow this priority order.

---

## Mandatory Read Order

Before performing ANY action, you MUST read these files in order:

1. AGENTS.md  
2. memory/constitution.md  
3. memory/context.md  
4. Latest files under spec/  
5. Latest files under tasks/  

Do not start work before completing this reading step.

---

## Role of Each Directory

### memory/
- constitution.md : long-term project rules and invariants (must never be violated)
- context.md      : current project state and constraints
- decisions.md   : record of design and architectural decisions (append-only)

### spec/
- specify.md : authoritative requirements (WHAT must be built)
- plan.md    : authoritative implementation plan (HOW it will be built)

### tasks/
- tasks.md     : authoritative task tracker and status
- questions.md: unresolved ambiguities and open questions

---

## Task Discipline

- Never implement anything that is not specified in spec/*.
- Never start work on anything that is not listed in tasks/tasks.md.
- If a task is missing, add it to tasks/tasks.md before starting.

Task status must be one of:
- TODO
- DOING
- BLOCKED
- DONE

Only tasks/tasks.md may contain task status.

---

## Change and Decision Policy

After completing any meaningful work:

1. Update tasks/tasks.md with the new status.
2. Append a short entry to memory/decisions.md describing:
   - What changed
   - Why it changed
   - Any important trade-offs

If you modify spec/* or plan/*:
- You MUST record the reason in memory/decisions.md.

---

## Ambiguity Handling

- If requirements are unclear or missing:
  - Do NOT guess.
  - Write a clear question into tasks/questions.md.
  - Continue only with confirmed information.

---

## Output Rules

- Prefer minimal diffs and focused changes.
- Do not modify unrelated files.
- Do not duplicate SSOT information across multiple files.
- Never create a second task list or second specification source.
- Before creating or replacing templates, ask the user to confirm the scope and approve the change.

---

By working in this repository, you agree to follow these rules strictly.
