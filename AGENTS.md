# REAL Color Mate - AI Development Guide

Version: 2.0  
Last Updated: 2026-08-04

---

## Purpose

REAL Color Mate is an open hardware project that assists automotive paint color matching by measuring spectral information and providing practical color analysis.

The objective is to build a portable, manufacturable, and maintainable device for real-world body shop use.

This project is NOT intended to copy or reverse engineer commercial color matching systems.

Every contribution should move the project toward a manufacturable product.

---

## Single Source of Truth

**MASTER_SPECIFICATION.md is the Single Source of Truth.**

All official project specifications, hardware configuration, software stack, optical specifications, and component verification rules are defined in:

> [MASTER_SPECIFICATION.md](./MASTER_SPECIFICATION.md)

AI assistants must always read these files in order before making design decisions:

1. **MASTER_SPECIFICATION.md** - Official project specifications
2. **CHANGELOG.md** - Official history of all design changes
3. **Related design documents** - Context and implementation details

Do not modify the project specification without explicit user approval.

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
- Include version numbers
- Keep documentation synchronized
- Explain assumptions
- Clearly distinguish verified information from assumptions
- Mark temporary designs as "Concept Design"
- Keep all project files internally consistent

### Never

- Guess specifications
- Invent dimensions
- Invent electrical characteristics
- Invent calibration values
- Invent component performance
- Change project architecture without approval
- Replace existing work without explanation
- Remove existing functionality without approval
- Use obsolete or unavailable components when practical alternatives exist

### If Information is Unavailable

Explicitly state: **Unknown**

- Explain why
- Suggest how to verify it

Never fabricate technical information.

---

## Design Philosophy

The project should be manufacturable using commonly available tools and services.

Examples include:

- JLCPCB
- PCBWay
- Commercial PCB manufacturers
- Commercial 3D printing services

Every design should be realistically manufacturable.

---

## Design Stages

### Concept Design

- Estimated dimensions allowed
- Placeholder models allowed
- Experimental ideas allowed

### Production Design

- Measured dimensions only
- Verified components only
- Manufacturing-ready data
- Complete documentation

Never confuse these two stages.

---

## Hardware and Software Specifications

For complete hardware and software specifications, see:

> [MASTER_SPECIFICATION.md - Hardware Specification](./MASTER_SPECIFICATION.md#hardware-specification)
> 
> [MASTER_SPECIFICATION.md - Software Stack](./MASTER_SPECIFICATION.md#software-stack)

Key components are documented in the official specification.

---

## Repository Structure

For the official repository structure, see:

> [MASTER_SPECIFICATION.md - Repository Structure](./MASTER_SPECIFICATION.md#repository-structure)

---

## File Responsibilities

| File | Purpose |
|------|---------|
| MASTER_SPECIFICATION.md | Official specifications (authority) |
| CHANGELOG.md | All approved changes and version history |
| docs/ | Design documents, calculations, research |
| hardware/ | KiCad schematics, PCB layouts |
| software/ | ESP32 firmware source code |
| mechanical/ | OpenSCAD, STEP, STL models |
| calibration/ | Calibration data and procedures |
| manufacturing/ | Manufacturing instructions |
| tools/ | Development utilities |
| BOM.md | Parts list and procurement |

---

## AI Collaboration

This repository is intended for collaborative development using multiple AI assistants.

Examples include:

- ChatGPT
- Google Gemini
- GitHub Copilot

Every AI assistant must follow the same specification (MASTER_SPECIFICATION.md).

No AI has authority to redefine project requirements.

Suggestions should be presented as proposals, not decisions.

---

## AI Responsibilities

| Assistant | Responsibility |
|-----------|-----------------|
| **ChatGPT** | Architecture, Documentation, OpenSCAD, Firmware Design, Project Management |
| **Google Gemini** | Mathematics, Color Science, Algorithm Review, Data Analysis |
| **GitHub Copilot** | Implementation, Code Completion, Refactoring, Unit Tests, Code Review |

All assistants must respect previous work and maintain consistency.

---

## Workflow

1. Read **MASTER_SPECIFICATION.md**
2. Read **CHANGELOG.md**
3. Review related files
4. Implement requested task
5. Update documentation
6. Update **CHANGELOG.md**
7. Produce deliverables

---

## Deliverables

Whenever applicable, produce actual files:

- Arduino Source Code
- ESP32 Firmware
- KiCad Project
- PCB Gerber Files
- Bill of Materials (BOM)
- OpenSCAD Models
- STL Files
- STEP Files
- CSV Data Files
- Calibration Files
- Documentation
- Diagrams

Avoid delivering explanation only.

---

## Versioning

Every deliverable should include a version number:

- **v0.1** - Concept Design
- **v0.5** - Prototype
- **v1.0** - Production Release

For complete versioning standards, see:

> [MASTER_SPECIFICATION.md - Versioning Standard](./MASTER_SPECIFICATION.md#versioning-standard)

---

## Documentation Standard

Documentation should be:

- Clear
- Reproducible
- Technically accurate
- Manufacturing-oriented

Avoid unnecessary verbosity.

---

## Error Handling

If information cannot be verified:

- State that it is **Unknown**
- Explain why
- Suggest how to verify it

Never fabricate technical information.

---

## Quality Checklist

Before completing any task, verify:

- □ MASTER_SPECIFICATION.md read and understood
- □ Specifications followed
- □ No guessed values
- □ Files remain consistent
- □ Documentation updated
- □ Version updated
- □ CHANGELOG updated
- □ Manufacturable output
- □ Deliverables are actual files

---

## Final Objective

The final objective is to create a practical, portable automotive paint measurement system that can be reproduced by third parties using the published manufacturing data.

Every contribution should move the project closer to that objective.
