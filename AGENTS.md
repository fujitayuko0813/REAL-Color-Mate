# REAL Color Mate - AI Development Guide
Version: 1.0
Last Updated: 2026-07-29

---

# Purpose

REAL Color Mate is an open hardware project that assists automotive paint color matching by measuring spectral information and providing practical color analysis.

The objective is to build a portable, manufacturable, and maintainable device for real-world body shop use.

This project is NOT intended to copy or reverse engineer commercial color matching systems.

Every contribution should move the project toward a manufacturable product.

---

# Single Source of Truth

The following files define the project.

1. Master_Specification.md
   Official project specification.

2. CHANGELOG.md
   Official history of all design changes.

3. Development_Log.md
   Development notes and implementation history.

AI assistants must always read these files before making design decisions.

Do not modify the project specification without explicit user approval.

---

# Core Principles

Always prioritize:

- Practicality
- Manufacturability
- Maintainability
- Repeatability
- Verified information
- Consistency

Never prioritize unnecessary complexity over usability.

---

# Development Rules

Always

- Read Master_Specification.md before starting work.
- Read CHANGELOG.md before implementing changes.
- Produce actual deliverables whenever possible.
- Include version numbers.
- Keep documentation synchronized.
- Explain assumptions.
- Clearly distinguish verified information from assumptions.
- Mark temporary designs as "Concept Design".
- Keep all project files internally consistent.

Never

- Guess specifications.
- Invent dimensions.
- Invent electrical characteristics.
- Invent calibration values.
- Invent component performance.
- Change project architecture without approval.
- Replace existing work without explanation.
- Remove existing functionality without approval.
- Use obsolete or unavailable components when practical alternatives exist.

If information is unavailable, explicitly state:

Unknown

instead of guessing.

---

# Design Philosophy

The project should be manufacturable using commonly available tools and services.

Examples include:

- JLCPCB
- PCBWay
- Commercial PCB manufacturers
- Commercial 3D printing services

Every design should be realistically manufacturable.

---

# Concept vs Production

Concept Design

- Estimated dimensions allowed
- Placeholder models allowed
- Experimental ideas allowed

Production Design

- Measured dimensions only
- Verified components only
- Manufacturing-ready data
- Complete documentation

Never confuse these two stages.

---

# Hardware Platform

MCU

ESP32-WROOM-32

Color Sensor

Adafruit AS7341

LED

Cree XP-G4

LED Driver

STMicroelectronics ALED8102

Power

5V

Storage

microSD

---

# Software Stack

Arduino IDE

ESP32 Arduino Framework

KiCad

OpenSCAD

CSV

Git

GitHub

---

# Optical System

45° illumination

0° observation

LED ring illumination

Matte black optical chamber

Replaceable measurement hood

Support both

- Vehicle measurement
- Test panel measurement

---

# Repository Structure

Hardware/

Firmware/

Mechanical/

BOM/

Documents/

Images/

TestData/

Calibration/

---

# File Responsibilities

Master_Specification.md

Official specifications

CHANGELOG.md

All approved changes

Development_Log.md

Daily work log

BOM/

Parts list

Hardware/

KiCad
Schematics
PCB

Firmware/

ESP32 source code

Mechanical/

OpenSCAD
STEP
STL

Documents/

Design documents
Calculations
Research

---

# AI Collaboration

This repository is intended for collaborative development using multiple AI assistants.

Examples include

- ChatGPT
- Google Gemini
- GitHub Copilot

Every AI assistant must follow the same specification.

No AI has authority to redefine project requirements.

Suggestions should be presented as proposals, not decisions.

---

# AI Responsibilities

ChatGPT

- Architecture
- Documentation
- OpenSCAD
- Firmware Design
- Project Management

Gemini

- Mathematics
- Color Science
- Algorithm Review
- Data Analysis

GitHub Copilot

- Implementation
- Refactoring
- Code Completion
- Unit Tests

All assistants must respect previous work.

---

# Workflow

1. Read Master_Specification.md

2. Read CHANGELOG.md

3. Review related files

4. Implement requested task

5. Update documentation

6. Update CHANGELOG.md

7. Produce deliverables

---

# Deliverables

Whenever applicable, produce actual files.

Examples

- Arduino Source
- ESP32 Firmware
- KiCad Project
- PCB
- Gerber
- BOM
- OpenSCAD
- STL
- STEP
- CSV
- Calibration Files
- Documentation
- Diagrams

Avoid delivering explanation only.

---

# Versioning

Every deliverable should include a version number.

Examples

v0.1 Concept

v0.5 Prototype

v1.0 Production

---

# Documentation Standard

Documentation should be

- Clear
- Reproducible
- Technically accurate
- Manufacturing-oriented

Avoid unnecessary verbosity.

---

# Error Handling

If information cannot be verified:

- State that it is Unknown.
- Explain why.
- Suggest how to verify it.

Never fabricate technical information.

---

# Quality Checklist

Before completing any task, verify:

□ Specifications followed

□ No guessed values

□ Files remain consistent

□ Documentation updated

□ Version updated

□ CHANGELOG updated

□ Manufacturable output

---

# Final Objective

The final objective is to create a practical, portable automotive paint measurement system that can be reproduced by third parties using the published manufacturing data.

Every contribution should move the project closer to that objective.
