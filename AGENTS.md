# REAL Color Mate - AI Development Guide

Version: 2.1  
Last Updated: 2026-08-26

---

## Purpose

REAL Color Mate is an open hardware project that assists automotive paint color matching by measuring spectral information and providing practical color analysis.

The objective is to build a portable, manufacturable, and maintainable device for real-world body shop use.

This project is NOT intended to copy or reverse engineer commercial color matching systems.

Every contribution should move the project toward a manufacturable product.

---

## Single Source of Truth

**MASTER_SPECIFICATION.md is the Single Source of Truth.**

All formal project specifications are defined in:

> [MASTER_SPECIFICATION.md](./MASTER_SPECIFICATION.md)

AI assistants must read these files in order before making design decisions:

1. **MASTER_SPECIFICATION.md** - Official project specifications
2. **CHANGELOG.md** - Approved change history
3. **Related design documents** - Context and implementation details

No AI assistant may change a decided specification without explicit project-owner approval.

---

## Core Principles

Always prioritize:

- Practicality
- Manufacturability
- Maintainability
- Repeatability
- Verified information
- Consistency

Never prioritize unnecessary complexity over usability.

---

## Development Rules

### Always

- Read **MASTER_SPECIFICATION.md** before starting work
- Read **CHANGELOG.md** before implementing changes
- Produce actual deliverables whenever possible
- Keep documentation synchronized
- Clearly distinguish verified information from assumptions
- Mark temporary designs as **Concept Design**
- Keep all project files internally consistent
- Update CHANGELOG.md when an approved project change is made

### Never

- Guess specifications
- Invent dimensions
- Invent electrical characteristics
- Invent calibration values
- Invent component performance
- Change project architecture without approval
- Replace existing work without explanation
- Remove existing functionality without approval

### If Information is Unavailable

Explicitly state: **Unknown**.

Explain why it is unknown and, where useful, state how it can be verified.

Never fabricate technical information.

---

## Design Stages

### Concept Design

- Estimated dimensions allowed
- Placeholder models allowed
- Experimental ideas allowed
- Must be clearly marked **Concept Design**

### Production Design

- Measured dimensions only
- Verified components only
- Manufacturing-ready data
- Complete documentation

Never confuse these two stages.

---

## Hardware and Software Specifications

For complete specifications, see:

> [MASTER_SPECIFICATION.md — Hardware Specification](./MASTER_SPECIFICATION.md#hardware-specification)
>
> [MASTER_SPECIFICATION.md — Software Stack](./MASTER_SPECIFICATION.md#software-stack)

---

## Repository Structure

Repository layout is an operational/documentation concern, not a formal product specification.

See:

> [docs/repository.md](./docs/repository.md)

Keep repository-layout references synchronized when directories or top-level documents change.

---

## File Responsibilities

| File / Directory | Purpose |
|---|---|
| MASTER_SPECIFICATION.md | Official specifications (authority) |
| CHANGELOG.md | Approved project/document changes and version history |
| ROADMAP.md | Planned development work |
| IDEA.md | Future ideas and proposals |
| docs/ | Design rationale, component selection, technical documentation and research |
| hardware/ | KiCad schematics and PCB layouts |
| software/ | ESP32 firmware |
| mechanical/ | OpenSCAD and mechanical design files |
| calibration/ | Calibration procedures and calibration data |
| manufacturing/ | Manufacturing instructions and production data |
| tools/ | Development utilities |
| BOM.md | Parts list and procurement |

---

## AI Collaboration

This repository supports collaborative development using ChatGPT, Google Gemini, and GitHub Copilot.

All assistants follow the same formal specification: **MASTER_SPECIFICATION.md**.

No AI has authority to redefine project requirements.

Suggestions must be presented as proposals, not decisions.

### Suggested Responsibilities

| Assistant | Responsibility |
|---|---|
| ChatGPT | Architecture, documentation, OpenSCAD, firmware design, project management |
| Google Gemini | Mathematics, color science, algorithm review, data analysis |
| GitHub Copilot | Implementation, code completion, refactoring, unit tests, code review |

These responsibilities are workflow guidance, not project specifications.

---

## Workflow

1. Read **MASTER_SPECIFICATION.md**
2. Read **CHANGELOG.md**
3. Review related files
4. Implement the requested task
5. Test where applicable
6. Update affected documentation
7. Update **CHANGELOG.md** for approved project changes
8. Produce deliverables

---

## Versioning

Versioning is an operational convention. Current release-stage labels are:

- **v0.1** - Concept Design
- **v0.5** - Prototype
- **v1.0** - Production Release

Do not treat this convention as a product specification.

---

## Documentation Standard

Documentation should be:

- Clear
- Reproducible
- Technically accurate
- Manufacturing-oriented
- Explicit about Unknown values

Avoid unnecessary verbosity.

---

## Quality Checklist

Before completing a task, verify:

- [ ] MASTER_SPECIFICATION.md read and understood
- [ ] CHANGELOG.md read
- [ ] Specifications followed
- [ ] No guessed values
- [ ] Files remain internally consistent
- [ ] Relevant documentation updated
- [ ] CHANGELOG updated when required
- [ ] Deliverables are actual files
- [ ] Output is clearly marked Concept Design when applicable

---

## Final Objective

Create a practical, portable automotive paint measurement system that can be reproduced by third parties using the published manufacturing data.

Every contribution should move the project closer to that objective.
