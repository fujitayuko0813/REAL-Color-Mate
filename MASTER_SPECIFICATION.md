# REAL Color Mate - Master Specification v2.0

**Last Updated:** 2026-08-03  
**Status:** Active Development  
**Version:** v2.0

---

## Document Purpose

This is the **single source of truth** for REAL Color Mate project specifications.

**Only DECIDED FACTS are recorded here.**
- Candidates, ideas, and future plans are NOT included.
- For ideas, see [IDEA.md](./IDEA.md)
- For development plans, see [ROADMAP.md](./ROADMAP.md)

---

## Project Overview

**Project Name:** REAL Color Mate  
**Full Name:** Portable Color Measurement Tool for Automotive Paint Matching  
**Primary Purpose:** Measure spectral information for automotive paint color matching  
**Target User:** Automotive body shops  
**Design Philosophy:** Practical, manufacturable, maintainable

### Core Objective
Create a portable, reproducible automotive paint measurement system using commonly available manufacturing services (JLCPCB, PCBWay, commercial 3D printing).

---

## Hardware Specification

### Microcontroller (MCU)
- **Component:** ESP32-WROOM-32
- **Function:** Main controller
- **Status:** Decided

### Color Sensor
- **Component:** Adafruit AS7341
- **Function:** Spectral measurement (11 channels)
- **Status:** Decided

### LED Illumination
- **Type:** LED Ring Illumination
- **Component:** Cree XP-G4
- **Driver:** STMicroelectronics ALED8102
- **Configuration:** 45° illumination, 0° observation angle
- **Status:** Decided

### Power Supply
- **Voltage:** 5V
- **Status:** Decided

### Storage
- **Type:** microSD Card
- **Function:** Data logging
- **Status:** Decided

### Optical System
- **Illumination Angle:** 45°
- **Observation Angle:** 0°
- **Chamber:** Matte black optical chamber
- **Measurement Hood:** Replaceable
- **Supported Measurements:**
  - Vehicle surface measurement
  - Test panel measurement
- **Status:** Decided

---

## Software Stack

| Component | Technology | Status |
|-----------|-----------|--------|
| IDE | Arduino IDE | Decided |
| Framework | ESP32 Arduino Framework | Decided |
| PCB Design | KiCad | Decided |
| 3D Design | OpenSCAD | Decided |
| Data Format | CSV | Decided |
| Version Control | Git / GitHub | Decided |

---

## Repository Structure

```
REAL-Color-Mate/
├── hardware/          # KiCad PCB design
├── software/          # ESP32 firmware
├── mechanical/        # OpenSCAD / STEP / STL
├── calibration/       # Calibration data and procedures
├── docs/              # Design documents and research
├── manufacturing/     # Manufacturing instructions
├── tools/             # Development tools
├── BOM.md             # Bill of materials
├── MASTER_SPECIFICATION.md    # This file
├── README.md          # Project overview
├── ROADMAP.md         # Development roadmap
├── IDEA.md            # Future ideas
├── CHANGELOG.md       # Version history
├── AGENTS.md          # AI collaboration rules
└── .github/
    └── copilot-instructions.md # AI behavior rules
```

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

---

## Component Verification Rules

The following must NOT be guessed or invented:
- Dimensions (use measured values only)
- Electrical characteristics
- Calibration values
- Component performance specifications

If information is unavailable: **Unknown**

---

## Compliance and Quality

### Development Rules - Always
- Read MASTER_SPECIFICATION.md before starting work
- Read CHANGELOG.md before implementing changes
- Produce actual deliverables whenever possible
- Include version numbers in all outputs
- Keep documentation synchronized
- Clearly distinguish verified facts from assumptions
- Mark temporary designs as "Concept Design"
- Keep all project files internally consistent

### Development Rules - Never
- Guess specifications
- Invent dimensions, electrical characteristics, or calibration values
- Invent component performance
- Change project architecture without approval
- Replace existing work without explanation
- Remove existing functionality without approval
- Use obsolete or unavailable components when practical alternatives exist

---

## Versioning Standard

| Version | Stage | Description |
|---------|-------|-------------|
| v0.1 | Concept | Initial prototype concept |
| v0.5 | Prototype | Working prototype with testing |
| v1.0 | Production | Manufacturing-ready release |

---

## File Responsibilities

| File | Purpose | Owner |
|------|---------|-------|
| MASTER_SPECIFICATION.md | Official specifications (DECIDED FACTS ONLY) | Project Lead |
| README.md | Project overview and quick start | Project Lead |
| ROADMAP.md | Development timeline and planned features | Project Team |
| IDEA.md | Future ideas and candidates | Project Team |
| CHANGELOG.md | All approved changes and versions | Project Lead |
| AGENTS.md | AI collaboration rules and guidelines | Project Lead |
| .github/copilot-instructions.md | AI behavior rules (sync with AGENTS.md) | Project Lead |
| BOM.md | Bill of materials with part numbers | Hardware Team |
| hardware/ | KiCad schematics and PCB | Hardware Team |
| software/ | ESP32 firmware source code | Software Team |
| mechanical/ | OpenSCAD, STEP, STL files | Mechanical Team |
| calibration/ | Calibration procedures and data | Test Team |
| manufacturing/ | Manufacturing and assembly instructions | Manufacturing Team |
| docs/ | Design documents and calculations | Documentation Team |

---

## Current Status

- **Hardware Design:** Concept stage (v0.1)
- **Firmware:** Not yet started
- **Mechanical Design:** Not yet started
- **Calibration:** Not yet started
- **Manufacturing:** Not yet started

---

## Known Constraints

Unknown - To be determined in ROADMAP.md

---

## AI Collaboration Policy

### Specification Authority
- MASTER_SPECIFICATION.md is immutable without explicit user approval
- Suggestions for changes must include: rationale, benefits, drawbacks, and impact scope
- AI assistants cannot modify specifications independently

### Required Reading
All AI assistants must read in this order:
1. MASTER_SPECIFICATION.md
2. CHANGELOG.md
3. Related design documents

### Workflow
1. Read MASTER_SPECIFICATION.md
2. Read CHANGELOG.md
3. Review related files
4. Implement requested task
5. Update documentation
6. Update CHANGELOG.md
7. Produce deliverables

---

## Document History

| Date | Version | Notes |
|------|---------|-------|
| 2026-08-03 | v2.0 | Initial creation: reorganized from AGENTS.md |

