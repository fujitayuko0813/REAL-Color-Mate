# REAL Color Mate

# Component Selection

## Purpose

This document records component-selection history and the current verification status of components used or considered for REAL Color Mate Version 2.x.

This is **not** a formal specification.

The authoritative specification is [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md).

The current BOM is recorded in [BOM.md](../BOM.md).

Selection history must not be used to redefine the formal specification.

---

## Selection Status Definitions

| Status | Meaning |
|---|---|
| Selected | The component is identified as selected in the current project documentation. |
| Purchased | The component is recorded as purchased. This does not by itself establish every mechanical or electrical characteristic. |
| Candidate | A component considered as a possible option, but not confirmed as selected. |
| Rejected | A component explicitly recorded as rejected. |
| Unknown | The available project documentation does not provide enough information to classify the item. |

---

## Component Selection Log

Only information verifiable from the current repository is recorded below. Selection rationale, alternatives, price, availability, and selection dates are marked `Unknown` where the repository does not provide that information.

### MCU-01 — ESP32-S3 DevKitC-1 N16R8

- **Manufacturer:** Espressif
- **Part Number / Module:** ESP32-S3-WROOM-1 N16R8
- **Category:** Microcontroller
- **Function:** Main controller
- **Selection Status:** Purchased / Selected
- **Selection Date:** Unknown
- **Reason for Selection:** Unknown
- **Alternatives Considered:** Unknown
- **Advantages:** Unknown
- **Disadvantages:** Unknown
- **Availability:** Purchased; current repository does not provide further availability information
- **Datasheet / Reference:** Unknown
- **Related Files:** [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md), [BOM.md](../BOM.md)
- **Notes:** Current MASTER_SPECIFICATION identifies this MCU as decided. Exact board dimensions remain unverified.

### SEN-01 — Adafruit AS7341

- **Manufacturer:** Adafruit
- **Part Number:** AS7341
- **Category:** Spectral sensor
- **Function:** Spectral measurement
- **Selection Status:** Purchased / Selected
- **Selection Date:** Unknown
- **Reason for Selection:** Unknown
- **Alternatives Considered:** Unknown
- **Advantages:** Unknown
- **Disadvantages:** Unknown
- **Availability:** Purchased; current repository does not provide further availability information
- **Datasheet / Reference:** Unknown
- **Related Files:** [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md), [BOM.md](../BOM.md)
- **Notes:** Channel definition is explicitly recorded as Unknown until verified against the exact purchased component documentation.

### LED-01 — Cree XP-G4

- **Manufacturer:** Cree LED
- **Part Number:** XPGEWT-02-0000-00000UHE3
- **Category:** White LED
- **Function:** LED ring illumination
- **Selection Status:** Purchased / Selected
- **Selection Date:** Unknown
- **Reason for Selection:** Unknown
- **Alternatives Considered:** Unknown
- **Advantages:** Unknown
- **Disadvantages:** Unknown
- **Availability:** Purchased
- **Datasheet / Reference:** Unknown
- **Related Files:** [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md), [BOM.md](../BOM.md)
- **Notes:** BOM records 12 purchased, with 8 used and 4 spare. Optical/mechanical placement distance remains to be determined during optical design and verification.

### DRV-01 — ALED8102SXTTR

- **Manufacturer:** STMicroelectronics
- **Part Number:** ALED8102SXTTR
- **Category:** LED driver
- **Function:** LED drive
- **Selection Status:** Purchased / Selected
- **Selection Date:** Unknown
- **Reason for Selection:** Unknown
- **Alternatives Considered:** Unknown
- **Advantages:** Unknown
- **Disadvantages:** Unknown
- **Availability:** Purchased
- **Datasheet / Reference:** Unknown
- **Related Files:** [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md), [BOM.md](../BOM.md)
- **Notes:** BOM records 2 purchased, with 1 used and 1 spare.

### LCD-01 — Makerbase MKS MINI12864 V3

- **Manufacturer:** Makerbase
- **Part Number:** MKS MINI12864 V3
- **Category:** Display / user interface
- **Function:** Display and user interface
- **Selection Status:** Purchased / Selected
- **Selection Date:** Unknown
- **Reason for Selection:** Unknown
- **Alternatives Considered:** Unknown
- **Advantages:** Unknown
- **Disadvantages:** Unknown
- **Availability:** Purchased
- **Datasheet / Reference:** Unknown
- **Related Files:** [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md), [BOM.md](../BOM.md)
- **Notes:** Mechanical dimensions and display-controller information remain Unknown until verified from the purchased module.

---

## Candidate Components

No candidate components are explicitly documented in the current repository sources reviewed for this document.

Do not add historical candidates from memory or external knowledge without a source in the project documentation.

---

## Rejected Components

No rejected components are explicitly documented in the current repository sources reviewed for this document.

---

## Unknown / Verification Required

The following information is not established by the current repository and must not be inferred:

| Component / Item | Unknown Information | Required Verification |
|---|---|---|
| ESP32-S3 DevKitC-1 N16R8 | Exact board dimensions | Measure purchased board |
| AS7341 | Exact channel definition for the purchased component/module | Verify exact purchased component documentation |
| Cree XP-G4 | Optical/mechanical placement distance | Determine during optical design and verification |
| MKS MINI12864 V3 | Exact mechanical dimensions | Measure purchased module |
| MKS MINI12864 V3 | Display controller | Verify from purchased module documentation |
| All listed components | Selection date and detailed selection rationale | Recover only from verifiable project records |

---

## Selection Decision Index

| ID | Component | Status | Category |
|---|---|---|---|
| MCU-01 | ESP32-S3 DevKitC-1 N16R8 | Purchased / Selected | Microcontroller |
| SEN-01 | Adafruit AS7341 | Purchased / Selected | Spectral sensor |
| LED-01 | Cree XP-G4 | Purchased / Selected | White LED |
| DRV-01 | ALED8102SXTTR | Purchased / Selected | LED driver |
| LCD-01 | Makerbase MKS MINI12864 V3 | Purchased / Selected | Display / UI |

---

## Source Documents

- [MASTER_SPECIFICATION.md](../MASTER_SPECIFICATION.md) — authoritative specification
- [BOM.md](../BOM.md) — current bill of materials
- [docs/design_history.md](./design_history.md) — design rationale and decision history

---

## Rules

- Do not invent component specifications.
- Do not infer selection rationale when it is not documented.
- Do not infer price or availability.
- Do not promote a candidate to Selected without verifiable project evidence.
- Do not use this document to change the formal specification.
- If information cannot be verified, write `Unknown`.
