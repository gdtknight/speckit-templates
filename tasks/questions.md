# Open Questions

This file contains unresolved questions and ambiguities.
Agents must NOT guess answers; they must record questions here.

---

## Q-001

Question:
- ...

Context:
- Where this uncertainty arises:

Impact:
- What is blocked or unclear because of this:

Status:
- Open / Answered

Resolution (when answered):
- ...

---

## Q-002

Question:
- Where are the speckit command templates stored in this repo (paths or directories)?
- Should the AGENTS.md compliance guidance be inserted verbatim from `AGENTS.md`, or do you have preferred wording?

Context:
- Current repository only contains placeholder template files and no obvious speckit command templates.

Impact:
- Cannot update speckit command templates without knowing where they live and the desired phrasing scope.

Status:
- Answered

Resolution (when answered):
- Speckit command templates contain AGENTS.md compliance guidance and follow the mandatory read order.

---

## Q-003

Question:
- Should we commit all `.codex/` contents (including `auth.json`, `history.jsonl`, `sessions/*`, and logs), or only the reusable template prompts under `.codex/prompts`?
- Same question for other agent/tooling metadata that may contain machine- or user-specific data.

Context:
- The repository currently contains untracked agent/tooling metadata files that might be local or sensitive.

Impact:
- Commit scope and privacy risk depend on this decision.

Status:
- Answered

Resolution (when answered):
- Exclude sensitive/local agent metadata from commits; include only reusable templates (e.g., speckit prompts, .specify templates/scripts).
