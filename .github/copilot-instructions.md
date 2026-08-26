# GitHub Copilot Instructions

**Version:** 2.1  
**Last Updated:** 2026-08-26

---

## Purpose

This file defines how GitHub Copilot should work with the REAL Color Mate repository.

It is an operational instruction file, not a formal project specification.

The formal specification is [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md).

---

## Required Reading Order

Before starting work, read:

1. [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md) — formal specification and Single Source of Truth
2. [CHANGELOG.md](../CHANGELOG.md) — approved change history
3. [AGENTS.md](../AGENTS.md) — repository and AI operating rules
4. Related documentation under `docs/` when applicable

---

## Core Responsibilities

GitHub Copilot is primarily responsible for:

- Implementation
- Code completion
- Refactoring
- Unit tests
- Code review
- Repository documentation maintenance when explicitly requested

Copilot must not independently redefine project requirements or make unapproved architecture decisions.

---

## Critical Rules

### Specifications

- Do not modify `MASTER_SPECIFICATION.md` unless the project owner explicitly approves the specification change.
- Do not guess specifications.
- Do not invent dimensions, electrical characteristics, calibration values, or component performance.
- If information cannot be verified, write **Unknown**.

### Files and Documentation

- Preserve existing work unless a requested change requires modification.
- Keep related documentation internally consistent.
- Update `CHANGELOG.md` when an approved project/document change is made.
- Clearly distinguish verified information, assumptions, and Concept Design material.

### Design

Prioritize:

1. Practicality
2. Manufacturability
3. Maintainability
4. Repeatability
5. Verified information

---

## Repository Structure

Repository layout is documented separately because it is an operational/documentation concern rather than a formal product specification.

See:

> [docs/repository.md](../docs/repository.md)

Do not reference a nonexistent `Repository Structure` section in `MASTER_SPECIFICATION.md`.

---

## Hardware and Software Reference

For authoritative hardware and software information, always use:

> [MASTER_SPECIFICATION.md — Hardware Specification](../MASTER_SPECIFICATION.md#hardware-specification)
>
> [MASTER_SPECIFICATION.md — Software Stack](../MASTER_SPECIFICATION.md#software-stack)

Do not maintain an independent hardware specification in this file.

### Current Hardware Summary

| Component | Current documented value | Status |
|---|---|---|
| Microcontroller | ESP32-S3 DevKitC-1 N16R8 | Decided |
| Color Sensor | Adafruit AS7341 | Decided |
| LED | Cree XP-G4 | Decided |
| LED Driver | STMicroelectronics ALED8102SXTTR | Decided |
| Display / UI | Makerbase MKS MINI12864 V3 | Decided |
| Power | 5V | Decided |
| Storage | microSD Card | Decided |

For complete and authoritative details, use `MASTER_SPECIFICATION.md`.

---

## Documentation Responsibilities

| File | Responsibility |
|---|---|
| `MASTER_SPECIFICATION.md` | Formal specifications only |
| `CHANGELOG.md` | Approved changes and history |
| `ROADMAP.md` | Planned work |
| `IDEA.md` | Future ideas/proposals |
| `docs/design_history.md` | Design rationale and decision history |
| `docs/component_selection.md` | Component selection history and verification status |
| `docs/repository.md` | Repository layout and file responsibilities |
| `AGENTS.md` | General AI/repository operating rules |
| `.github/copilot-instructions.md` | Copilot-specific operating rules |

---

## Workflow

1. Read the required documentation in the order above.
2. Review relevant existing files.
3. Implement only the requested task.
4. Test where applicable.
5. Verify internal consistency.
6. Update affected documentation.
7. Update `CHANGELOG.md` when the change is approved and material.
8. Report changed files, verification results, and any remaining Unknown items.

---

## Error Handling

If information cannot be verified:

1. State **Unknown**.
2. Explain why it is unknown.
3. Suggest how it can be verified when useful.
4. Never fabricate technical information.

---

## Quality Gate

Before completing a task, verify:

- [ ] `MASTER_SPECIFICATION.md` read and followed
- [ ] `CHANGELOG.md` read
- [ ] `AGENTS.md` read
- [ ] No guessed or invented technical values
- [ ] Related files remain internally consistent
- [ ] Documentation updated where required
- [ ] `CHANGELOG.md` updated when required
- [ ] Deliverables are actual files
- [ ] Concept Design is clearly marked when applicable

---

## AI Collaboration

This project uses multiple AI assistants:

| Assistant | Primary role |
|---|---|
| GitHub Copilot | Implementation, code, refactoring, tests, code review |
| ChatGPT | Architecture, documentation, OpenSCAD, firmware design, project management |
| Google Gemini | Mathematics, color science, algorithm review, data analysis |

These are workflow roles, not authority over project specifications.

All assistants must follow `MASTER_SPECIFICATION.md`.

---

**Authority:** `MASTER_SPECIFICATION.md`  
**Reading Order:** `MASTER_SPECIFICATION.md` → `CHANGELOG.md` → `AGENTS.md`
