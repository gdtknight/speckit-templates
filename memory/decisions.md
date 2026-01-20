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

---

## [2026-01-21] Decision: Add AGENTS.md compliance guidance to speckit commands

Context:
- The user requested that speckit commands enforce AGENTS.md instructions across agents.

Decision:
- Insert AGENTS.md compliance guidance into speckit command templates for Codex, Gemini, and Copilot (and keep Claude aligned where present).

Rationale:
- Ensures all speckit-driven workflows follow the repository's mandatory read order.

Consequences:
- Speckit command templates now instruct agents to read AGENTS.md and related files before acting.

---

## [2026-01-21] Decision: Close Task-012 after verification

Context:
- Task-012 required confirming AGENTS.md compliance guidance in speckit command templates.

Decision:
- Verified the guidance exists across Codex, Gemini, and Copilot templates and marked Task-012 as DONE.

Rationale:
- The verification confirms the requirement is satisfied and the task can be closed.

Consequences:
- Task tracking reflects the completed compliance work.

---

## [2026-01-21] Decision: Mark Q-002 as answered

Context:
- Q-002 asked where speckit command templates live and what wording to use for AGENTS.md compliance.

Decision:
- Marked Q-002 as answered with the resolved guidance.

Rationale:
- Compliance wording and locations are now established in the templates.

Consequences:
- Questions log reflects the resolved ambiguity.

---

## [2026-01-21] Decision: Normalize task numbering

Context:
- Task IDs used mixed numbering that did not start at 001.

Decision:
- Renumbered existing tasks to use a consistent 001+ sequence.

Rationale:
- Keeps the template task list consistent and easier to follow.

Consequences:
- Task IDs were updated in `tasks/tasks.md`.

---

## [2026-01-21] Decision: Verify starter template readiness

Context:
- The user requested confirmation that the repository can serve as a starter template with shared agent references.

Decision:
- Verified repository structure and confirmed speckit prompts across agents reference the same SSOT files and AGENTS.md read order.

Rationale:
- Ensures consistent behavior across Codex, Gemini, Copilot, and Claude templates.

Consequences:
- Task-008 marked as done; no content changes required.

---

## [2026-01-21] Decision: Block Task-009 pending commit scope confirmation

Context:
- Preparing agent-separated conventional commits requires deciding whether to include local agent metadata files.

Decision:
- Blocked Task-009 and logged Q-003 to confirm commit scope for `.codex/` and similar tool metadata.

Rationale:
- Avoids committing potentially sensitive or machine-specific data without explicit approval.

Consequences:
- Commit work is paused until Q-003 is answered.

---

## [2026-01-21] Decision: Exclude sensitive agent metadata from commits

Context:
- Q-003 required deciding whether to commit local agent metadata such as `.codex/auth.json` and session logs.

Decision:
- Commit only reusable templates and exclude sensitive/local metadata files (including local configs and logs).

Rationale:
- Avoids leaking credentials or machine-specific artifacts into the template repository.

Consequences:
- Commit scope is limited to template-relevant files; Task-009 can proceed.

---

## [2026-01-21] Decision: Complete Task-009 with per-file commits

Context:
- Task-009 required agent-separated, per-file conventional commits for current changes.

Decision:
- Completed per-file commits across agent templates and other repository updates.

Rationale:
- Provides clean, auditable commit history for each template asset.

Consequences:
- Task-009 marked as done with granular commit history.
