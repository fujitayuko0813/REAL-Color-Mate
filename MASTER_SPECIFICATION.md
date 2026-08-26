# REAL Color Mate - Master Specification v2.1

**Last Updated:** 2026-08-27  
**Status:** Active Development  
**Version:** v2.1

---

## Document Purpose

This is the **single source of truth** for REAL Color Mate project specifications.

**Only DECIDED FACTS are recorded here.**
- Candidates, ideas, and future plans are NOT included.
- For ideas, see [IDEA.md](./IDEA.md)
- For development plans, see [ROADMAP.md](./ROADMAP.md)
- Design rationale is recorded in [docs/design_history.md](./docs/design_history.md)

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
- **Component:** ESP32-S3 DevKitC-1 N16R8
- **Module:** ESP32-S3-WROOM-1 N16R8
- **Function:** Main controller
- **Status:** Decided

### Color Sensor
- **Component:** Adafruit AS7341
- **Function:** Spectral measurement
- **Channel definition:** Unknown; must be verified against the exact purchased component documentation before being recorded as a fixed specification.
- **Status:** Decided

### LED Illumination
- **Type:** LED Ring Illumination
- **Component:** Cree XP-G4
- **Part Number:** XPGEWT-02-0000-00000UHE3
- **Quantity:** 8 used; 4 spare
- **Driver:** STMicroelectronics ALED8102SXTTR
- **Configuration:** 45° illumination, 0° observation angle
- **Status:** Decided

### Display / User Interface
- **Module:** Makerbase MKS MINI12864 V3
- **Function:** Display and user interface
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

### Included

- Spectral measurement
- XYZ conversion
- CIE Lab conversion
- DeltaE calculation
- Calibration
- CSV data logging

### Excluded

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

**MASTER_SPECIFICATION.md is the single, authoritative source of truth.**

Operational AI collaboration rules and workflows are defined in AGENTS.md.

No AI collaborator may change a decided specification without explicit project-owner approval.

---

## Document History

| Date | Version | Notes |
|------|---------|-------|
| 2026-08-27 | v2.1 | Added verified physical measurements for the actual Makerbase MKS MINI12864 V3 module and linked the detailed measurement record. |
| 2026-08-19 | v2.1 | Synchronized MCU and purchased hardware with approved BOM; removed unverified AS7341 channel count; normalized LED driver and LED part information |
| 2026-08-04 | v2.0 | Refactored: Separated specifications from operational rules |
| 2026-08-03 | v2.0 | Initial creation: reorganized from AGENTS.md |

---

## Display Module — Verified Measurement Record

**Module:** Makerbase MKS MINI12864 V3.0  
**Measurement status:** Actual hardware measured  
**Unit:** mm  
**Measurement method:** Digital caliper  
**Detailed record:** [docs/hardware/MKS_MINI12864_V3_MEASURED.md](./docs/hardware/MKS_MINI12864_V3_MEASURED.md)

### Encoder / Rotary Knob

| Item | Measured value | Notes |
|---|---:|---|
| Shaft diameter | **5.98 mm** | Actual shaft diameter |
| Shaft protrusion, PCB surface to shaft tip | **22.50 mm** | PCB front surface is the reference |
| Threaded section diameter at mounting-nut area | **6.80 mm** | Mounting nut was not available during measurement |
| Threaded section length | **5.10 mm** | |
| Knob outside diameter | **25.00 mm** | |
| Knob height, PCB surface to knob top | **24.50 mm** | PCB front surface is the reference |

### LCD

| Item | Measured value | Notes |
|---|---:|---|
| LCD glass width | **58.24 mm** | Overall glass dimension |
| LCD glass height | **39.00 mm** | Overall glass dimension |
| Active display area width | **53.00 mm** | |
| Active display area height | **28.68 mm** | |
| LCD protrusion, PCB surface to glass surface | **6.11 mm** | PCB front surface is the reference |

**Initial enclosure design opening:** 58.84 × 39.60 mm, based on approximately +0.30 mm clearance per side. This is a derived CAD design value, not a physical measurement.

### Reset Button

| Item | Measured value | Notes |
|---|---:|---|
| Button diameter | **3.40 mm** | |
| Button height, PCB surface to button top | **6.22 mm** | PCB front surface is the reference |
| Button center X from left PCB edge | **97.44 mm** | Left-edge reference |
| Button center Y from bottom PCB edge | **9.85 mm** | Bottom-edge reference |

### SD Card Slot

| Item | Measured value | Notes |
|---|---:|---|
| Card protrusion when fully inserted | **5.50 mm** | |
| Slot opening width | **28.70 mm** | |
| Slot opening height | **2.70 mm** | |
| Approximate card replacement space | **30.80 mm** | Practical design reference; not a precision tolerance |

### Rear-side Components

| Item | Measured value | Notes |
|---|---:|---|
| Maximum rear-side component height | **9.07 mm** | Rear-side reference |
| Connector height | **9.07 mm** | Rear-side reference |
| Pin-header length, PCB surface to pin tip | **20.50 mm** | Do not treat as component-body height |

### Spacer / PCB underside

The following are **not yet measured / not yet decided**:
- PCB underside to support surface / spacer height: **未測定**
- Component height around mounting holes on PCB underside: **未測定**
- Recommended spacer height: **未決定**

### Previously recorded board reference dimensions

These values were recorded earlier in the project and are **reference values, not newly measured values from this measurement session**:

- PCB overall size: **106.60 × 47.00 mm**
- Mounting holes: **4 × Ø3.20 mm**
- Horizontal mounting-hole center spacing: **93.00 mm**
- Vertical mounting-hole center spacing: **41.00 mm**
- Left edge to left hole center: **6.60 mm**
- Right edge to right hole center: **7.00 mm**
- Bottom edge to lower hole center: **3.00 mm**
- Top edge to upper hole center: **3.00 mm**
- PCB thickness: **1.60 mm** (reference)

### Approved Mechanical Design Policy

- Mechanical parts shall prioritize ease of assembly over tight cosmetic tolerances.
- Use practical clearances suitable for FDM 3D printing.
- A small visible gap is acceptable.
- PCB-to-enclosure clearance: approximately **0.5 mm** as the initial design rule.
- LCD window clearance: approximately **0.30 mm per side**.
- Encoder shall rotate freely without touching the enclosure.
- SD card shall be removable without disassembling the enclosure.
- Reset button shall remain operable after enclosure assembly.
- Optical components (AS7341, LED ring, measurement hood and optical chamber) are excluded from this relaxed clearance policy and require precision mechanical design.

### Measurement Reference Rules

- Front-side component heights use the **PCB front surface as the zero reference**.
- Reset button height is **PCB surface → button top**.
- Encoder knob height is **PCB surface → knob top**.
- Encoder shaft protrusion is **PCB surface → shaft tip**.
- LCD protrusion is **PCB surface → glass surface**.
- Rear-side measurements must use the specified PCB rear reference plane consistently.
- Measured values must not be replaced by catalog values unless explicitly marked as reference/catalog data.
- Unmeasured dimensions must not be inferred.
