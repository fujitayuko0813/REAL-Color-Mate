# Makerbase MKS MINI12864 V3 — 実測寸法記録

**Project:** REAL Color Mate  
**Module:** Makerbase MKS MINI12864 V3.0  
**Measurement status:** Actual hardware measurement completed for listed items  
**Unit:** mm  
**Measurement method:** Digital caliper  
**Recorded:** 2026-08-27  

> この文書は、REAL Color Mateの筐体・UI機構設計に使用するための実測寸法記録です。数値は実物をノギスで測定した値をそのまま記録しています。未測定項目は推測せず「未測定」としています。

## 1. Encoder / Rotary Knob

| No. | Measurement item | Measured value (mm) | Notes |
|---|---|---:|---|
| 1 | Shaft diameter | **5.98** | Actual shaft diameter |
| 2 | Shaft protrusion, PCB surface to shaft tip | **22.50** | Height reference is PCB front surface |
| 3 | Threaded section diameter at mounting-nut area | **6.80** | **No mounting nut available during measurement** |
| 4 | Threaded section length | **5.10** | |
| 5 | Knob outside diameter | **25.00** | |
| 6 | Knob height, PCB surface to knob top | **24.50** | Height reference is PCB front surface |

### Encoder design note
The enclosure shall provide enough clearance for free rotation of the knob. Cosmetic zero-clearance fitting is not required.

## 2. LCD

| No. | Measurement item | Measured value (mm) | Notes |
|---|---|---:|---|
| 1 | LCD glass width (overall) | **58.24** | Glass outer dimension |
| 2 | LCD glass height (overall) | **39.00** | Glass outer dimension |
| 3 | Active display area width | **53.00** | Actual visible/display area measured on module |
| 4 | Active display area height | **28.68** | Actual visible/display area measured on module |
| 5 | LCD protrusion, PCB surface to glass surface | **6.11** | Height reference is PCB front surface |

### LCD enclosure design rule
Use approximately **0.30 mm clearance per side** for the LCD window. This gives an initial enclosure opening target of approximately:

- Width: **58.84 mm**
- Height: **39.60 mm**

These are **design values derived from the measured values**, not additional physical measurements.

## 3. Reset Button

| No. | Measurement item | Measured value (mm) | Notes |
|---|---|---:|---|
| 1 | Button diameter | **3.40** | |
| 2 | Button height, PCB surface to button top | **6.22** | Height reference is PCB front surface |
| 3 | Button center X position from left PCB edge | **97.44** | Left-edge reference |
| 4 | Button center Y position from bottom PCB edge | **9.85** | Bottom-edge reference |

### Reset button design note
Button height is measured from the **PCB surface**, not from the button body/base. The enclosure should provide practical clearance for operation and printing tolerance.

## 4. SD Card Slot

| No. | Measurement item | Measured value (mm) | Notes |
|---|---|---:|---|
| 1 | Card protrusion when fully inserted | **5.50** | |
| 2 | Slot opening width | **28.70** | |
| 3 | Slot opening height | **2.70** | |
| 4 | Approximate space required for card replacement | **30.80** | Practical handling allowance measured/estimated during physical check; retain as a design reference rather than a precision dimension |

### SD card design rule
The card must remain removable without disassembling the enclosure. A small amount of visible gap around the opening is acceptable.

## 5. Rear-side Components

| No. | Measurement item | Measured value (mm) | Notes |
|---|---|---:|---|
| 1 | Maximum component height | **9.07** | PCB rear-side reference; measured highest rear component |
| 2 | Connector height | **9.07** | PCB rear-side reference |
| 3 | Pin-header length, PCB surface to pin tip | **20.50** | |

> **Important:** The rear-side height values are for enclosure internal clearance. Do not confuse the 20.50 mm pin-header length with component-body height.

## 6. Spacer / PCB underside

| No. | Measurement item | Status | Notes |
|---|---|---|---|
| 1 | PCB underside to table / support surface | **未測定** | Spacer height not yet finalized |
| 2 | Component height around mounting holes on PCB underside | **未測定** | Do not guess |
| 3 | Recommended spacer height | **未決定** | Determine after enclosure and mounting method are finalized |

## 7. Previously recorded board reference dimensions

The following dimensions were already recorded in the project as reference values. They are **not newly measured in this measurement session** and must be treated separately from the actual measured values above.

| Item | Reference value | Status |
|---|---:|---|
| PCB overall width | **106.60 mm** | Reference value |
| PCB overall height | **47.00 mm** | Reference value |
| Mounting hole diameter | **4 × Ø3.20 mm** | Reference value |
| Mounting-hole horizontal center spacing | **93.00 mm** | Reference value |
| Mounting-hole vertical center spacing | **41.00 mm** | Reference value |
| Left PCB edge to left mounting-hole center | **6.60 mm** | Reference value |
| Right PCB edge to right mounting-hole center | **7.00 mm** | Reference/calculated value |
| Bottom PCB edge to lower mounting-hole center | **3.00 mm** | Reference value |
| Top PCB edge to upper mounting-hole center | **3.00 mm** | Reference/calculated value |
| PCB thickness | **1.60 mm** | Reference value |

## 8. Approved mechanical design policy

For the REAL Color Mate prototype enclosure:

- **Assembly reliability has priority over minimum cosmetic gaps.**
- Practical clearance suitable for FDM 3D printing is preferred.
- A small visible gap is acceptable.
- PCB-to-enclosure clearance: approximately **0.5 mm** as the initial design rule.
- LCD window clearance: approximately **0.30 mm per side**.
- Encoder must rotate freely without touching the enclosure.
- SD card must be removable without disassembling the enclosure.
- Reset button must remain operable after enclosure assembly.
- Optical components (AS7341, LED ring, measurement hood and optical chamber) are **excluded** from this relaxed mechanical-clearance policy and require precision mechanical design.

## 9. Measurement reference rules

- For front-side component heights, use the **PCB front surface as the zero reference**.
- For rear-side component heights, use the **PCB rear surface / specified PCB reference plane** consistently.
- Reset button height is **PCB surface → button top**.
- Encoder knob height is **PCB surface → knob top**.
- Encoder shaft protrusion is **PCB surface → shaft tip**.
- LCD protrusion is **PCB surface → glass surface**.
- Do not replace measured values with catalog values unless explicitly marked as catalog/reference data.
- Do not infer unmeasured dimensions.

## 10. Data classification

**Measured from actual hardware:**
- Encoder: 6 values
- LCD: 5 values
- Reset button: 4 values
- SD slot: 4 values
- Rear-side components: 3 values

**Not yet measured / decided:**
- Spacer section: 3 values

**Reference values from earlier project documentation:**
- PCB overall dimensions
- Mounting-hole pattern
- PCB thickness

This distinction must be preserved in future CAD, KiCad, OpenSCAD, STEP and STL work.
