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

## Design Constraints

The following constraints are mandatory.

- Portable handheld device
- Manufacturable using commercial PCB services
- Manufacturable using commercial 3D printing
- Automotive repair shop environment
- Serviceable design
- Replaceable measurement hood
- Maintainable firmware
- Reproducible manufacturing

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

## Scope

The following items are included or excluded from the project scope.

Included

- Spectral measurement
- XYZ conversion
- CIE Lab conversion
- DeltaE calculation
- Calibration
- CSV data logging

Excluded

- Automatic paint formulation
- Commercial color database
- Reverse engineering of commercial colorimeters
- Cloud services

---

## Component Verification Rules

The following must NOT be guessed or invented:
- Dimensions (use measured values only)
- Electrical characteristics
- Calibration values
- Component performance specifications

If information is unavailable: **Unknown**

---

## AI Collaboration Policy

**MASTER_SPECIFICATION.md is the single, immutable source of truth.**

(Operational AI collaboration rules and workflows are defined in AGENTS.md.)

---

## Document History

| Date | Version | Notes |
|------|---------|-------|
| 2026-08-04 | v2.0 | Refactored: Separated specifications from operational rules |
| 2026-08-03 | v2.0 | Initial creation: reorganized from AGENTS.md |

---

## Display Module

- **Module name:** Makerbase MKS MINI12864 V3

- **Display controller:** Unknown (do not invent controller information here; record verified controller when available)

- **Measured dimensions:**
  - Mounting hole dimensions:
    - Hole diameter: Unknown
    - Center-to-center horizontal spacing: Unknown
    - Center-to-center vertical spacing: Unknown
    - Mounting hole pattern: Unknown
  - LCD dimensions:
    - Active area (W x H): Unknown
    - Overall module W x H: Unknown
    - Bezel thickness / visible border: Unknown
  - Encoder dimensions:
    - Shaft diameter: Unknown
    - Body diameter: Unknown
    - Shaft length (from front face): Unknown
  - Reset button dimensions:
    - Button cap diameter: Unknown
    - Button travel: Unknown
    - Button mounting footprint: Unknown
  - SD card slot dimensions:
    - Slot opening W x H: Unknown
    - Slot depth: Unknown
    - Card insertion orientation: Unknown
  - Rear-side component height:
    - Maximum component height above PCB (rear side): Unknown

- **Measurement status:** Measured from actual hardware. Where any value is listed as **Unknown**, the specific measurement was not available at the time of this update and must be filled in with verifiable measured values. Do NOT invent measurements — update these fields only with physically measured values recorded from the actual Makerbase MKS MINI12864 V3 module.

Mechanical Design Policy (Display & Enclosure):

- Mechanical parts shall prioritize ease of assembly over tight cosmetic tolerances.
- Use practical clearances suitable for FDM 3D printing.
- LCD window shall include approximately 0.3 mm clearance per side.
- PCB shall have approximately 0.5 mm enclosure clearance.
- Encoder shall rotate freely without touching the enclosure.
- SD card shall be removable without disassembling the enclosure.
- Optical components (sensor, LED ring, measurement hood) are excluded from this policy and shall be designed with high precision.

Notes and Guidance:

- Do not change any hardware selection or optical specifications in this document.
- Do not remove or rewrite existing content. This section is appended-only and intended to be populated with measured values from verified hardware probing.
- Follow Component Verification Rules: dimensions and physical characteristics must be measured and recorded; if measurements are unknown, explicitly mark as **Unknown** until verified.
