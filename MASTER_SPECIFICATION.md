# REAL Color Mate - Master Specification v2.0

**Last Updated:** 2026-08-04  
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

---

## Optical Specification

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
├── MASTER_SPECIFICATION.md    # This file (official specifications)
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

## Versioning Standard

| Version | Stage | Description |
|---------|-------|-------------|
| v0.1 | Concept | Initial prototype concept |
| v0.5 | Prototype | Working prototype with testing |
| v1.0 | Production | Manufacturing-ready release |

---

## Current Hardware / Software Configuration

- **ESP32 MCU:** ESP32-WROOM-32
- **Color Sensor:** Adafruit AS7341
- **LED Driver:** STMicroelectronics ALED8102
- **Power Supply:** 5V
- **Storage:** microSD Card
- **IDE:** Arduino IDE
- **Framework:** ESP32 Arduino Framework
- **PCB Design Tool:** KiCad
- **3D Design Tool:** OpenSCAD
- **Data Format:** CSV

---

## AI Collaboration Policy

### Specification Authority

**MASTER_SPECIFICATION.md is the single, immutable source of truth.**

- AI assistants must read MASTER_SPECIFICATION.md before starting any work
- Changes to specifications require explicit user approval
- Suggestions for changes must include: rationale, benefits, drawbacks, and impact scope
- AI assistants cannot modify specifications independently

### Required Reading Order

All AI assistants must read in this order:

1. **MASTER_SPECIFICATION.md** (Official specifications)
2. **CHANGELOG.md** (History of approved changes)
3. **Related design documents** (Context and details)

---

## Document History

| Date | Version | Notes |
|------|---------|-------|
| 2026-08-04 | v2.0 | Refactored: Separated specifications from operational rules |
| 2026-08-03 | v2.0 | Initial creation: reorganized from AGENTS.md |

