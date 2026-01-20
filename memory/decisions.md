# Design & Architecture Decisions

This file records important decisions and their rationale.
Entries are append-only and must never be deleted or rewritten.

---

## [YYYY-MM-DD] Decision: <short title>

Context:
- What problem or choice was being considered?

Decision:
- What was chosen?

Rationale:
- Why this option was selected.
- Trade-offs considered.

Consequences:
- Expected impact.
- Risks introduced.
- Follow-up actions (if any).

---

## [2026-01-20] Decision: Reset repository files to template placeholders

Context:
- The repository is being converted into a reusable template for new projects.
- The user requested that existing project-specific content be replaced with generic placeholders.

Decision:
- Replace memory, spec, and tasks files with neutral template content.
- Add a rule requiring user confirmation before creating or replacing templates.

Rationale:
- Ensures a clean, reusable baseline for new projects.
- Prevents unapproved template changes.

Consequences:
- Project-specific history is removed from template files.
- Future template changes must request confirmation first.
