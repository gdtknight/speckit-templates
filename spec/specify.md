# Specification

This document defines the authoritative requirements of the system.
This is the SINGLE source of truth for WHAT must be built.

---

## Problem Statement

Describe the problem this project is solving.

- Background:
- Motivation:
- Stakeholders:

---

## Goals

Primary goals:

- G1:
- G2:
- G3:

---

## Non-Goals

Explicitly out of scope:

- NG1:
- NG2:

---

## Functional Requirements

### FR-1: <short title>
- Description:
- Inputs:
- Outputs:
- Success criteria:
  - ...

### FR-2: Speckit command compliance
- Description: Speckit command templates must instruct supported agents to follow the mandatory read order in `AGENTS.md` before any action.
- Inputs: Speckit command invocation.
- Outputs: Agent guidance that enforces the read order.
- Success criteria:
  - All speckit command templates used by Codex, Gemini, Copilot, and Claude (when present) include the AGENTS.md compliance instruction.

---

## Non-Functional Requirements

- Performance:
  - ...
- Memory:
  - ...
- Reliability:
  - ...
- Portability:
  - ...

---

## Interfaces

- Public APIs:
  - ...

- External dependencies:
  - ...

---

## Constraints

- Language/version constraints:
- Library constraints:
- Platform constraints:

---

## Acceptance Criteria

The system is considered complete when:

- [ ] All functional requirements satisfied
- [ ] All non-functional requirements met
- [ ] Tests passing
- [ ] No critical known issues
