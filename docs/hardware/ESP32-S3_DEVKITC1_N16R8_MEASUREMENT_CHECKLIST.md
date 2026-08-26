# ESP32-S3 DevKitC-1 N16R8 — Physical Measurement Checklist

Version: 1.0
Date: 2026-08-27
Status: Measurement Required

## Purpose

This checklist contains **only measurements that should be taken from the purchased physical ESP32-S3 DevKitC-1 N16R8 board**.

Espressif documentation provides the board dimensions, PCB layout, schematic, and related design files. Therefore, values such as nominal PCB dimensions, hole locations, pin functions, connector types, and electrical specifications are intentionally excluded from this checklist. They should be treated as reference data, not re-measured unless a discrepancy is found.

Espressif documents both the initial ESP32-S3-DevKitC-1 and v1.1. The principal documented revision difference is the RGB LED GPIO assignment: GPIO48 on the initial version and GPIO38 on v1.1. Confirm the purchased board revision before recording measurements.

## Before Measuring

- [ ] Photograph the complete front side
- [ ] Photograph the complete rear side
- [ ] Photograph all markings and labels
- [ ] Record board revision if printed/identifiable
- [ ] Record the exact module marking: ESP32-S3-WROOM-1 N16R8
- [ ] Use a digital caliper where practical
- [ ] Do not force the caliper against connectors, shields, buttons, or fragile components
- [ ] Record measured values to 0.01 mm where the instrument permits
- [ ] If a value cannot be measured reliably, record `Unknown`

## A. Board-to-Case Critical Measurements

| ID | Measurement | Value | Unit | Notes |
|---|---|---:|---|---|
| ESP-M01 | Overall PCB length | ______ | mm | Physical edge to edge |
| ESP-M02 | Overall PCB width | ______ | mm | Physical edge to edge |
| ESP-M03 | PCB thickness | ______ | mm | Measure bare board edge if possible |
| ESP-M04 | Maximum component height above PCB | ______ | mm | Highest rigid component, excluding antenna clearance requirement |
| ESP-M05 | Maximum component height below PCB | ______ | mm | Measure underside protrusion |
| ESP-M06 | Maximum overall thickness including both sides | ______ | mm | Useful for enclosure stack-up |

## B. Mounting Geometry

| ID | Measurement | Value | Unit | Notes |
|---|---|---:|---|---|
| ESP-M07 | Mounting-hole diameter — hole 1 | ______ | mm | Verify against all holes |
| ESP-M08 | Mounting-hole diameter — hole 2 | ______ | mm | |
| ESP-M09 | Mounting-hole diameter — hole 3 | ______ | mm | |
| ESP-M10 | Mounting-hole diameter — hole 4 | ______ | mm | |
| ESP-M11 | Hole center-to-center, long axis | ______ | mm | Physical measurement |
| ESP-M12 | Hole center-to-center, short axis | ______ | mm | Physical measurement |
| ESP-M13 | Left PCB edge to nearest hole center | ______ | mm | Define left edge from component-side orientation |
| ESP-M14 | Right PCB edge to nearest hole center | ______ | mm | |
| ESP-M15 | Top PCB edge to nearest hole center | ______ | mm | |
| ESP-M16 | Bottom PCB edge to nearest hole center | ______ | mm | |

## C. Connector and Port Geometry

Measure the physical locations needed to make enclosure openings. Do not duplicate nominal connector specifications from the datasheet.

| ID | Measurement | Value | Unit | Notes |
|---|---|---:|---|---|
| ESP-M17 | USB-to-UART connector outer width | ______ | mm | Physical connector body |
| ESP-M18 | USB-to-UART connector outer height | ______ | mm | |
| ESP-M19 | USB-to-UART connector center from PCB edge | ______ | mm | Define reference edge |
| ESP-M20 | USB-to-UART connector protrusion beyond PCB edge | ______ | mm | |
| ESP-M21 | ESP32-S3 USB connector outer width | ______ | mm | If populated on purchased board |
| ESP-M22 | ESP32-S3 USB connector outer height | ______ | mm | |
| ESP-M23 | ESP32-S3 USB connector center from PCB edge | ______ | mm | |
| ESP-M24 | ESP32-S3 USB connector protrusion beyond PCB edge | ______ | mm | |
| ESP-M25 | Distance between the two USB connector bodies | ______ | mm | Case opening / plug clearance |

## D. Buttons and LEDs

| ID | Measurement | Value | Unit | Notes |
|---|---|---:|---|---|
| ESP-M26 | BOOT button center from PCB edge | ______ | mm | X reference |
| ESP-M27 | BOOT button center from PCB edge | ______ | mm | Y reference |
| ESP-M28 | BOOT button diameter/outer size | ______ | mm | Physical button cap |
| ESP-M29 | BOOT button maximum height above PCB | ______ | mm | |
| ESP-M30 | RESET/EN button center from PCB edge | ______ | mm | X reference |
| ESP-M31 | RESET/EN button center from PCB edge | ______ | mm | Y reference |
| ESP-M32 | RESET/EN button diameter/outer size | ______ | mm | |
| ESP-M33 | RESET/EN button maximum height above PCB | ______ | mm | |
| ESP-M34 | Power LED center from PCB edge | ______ | mm | If enclosure visibility matters |
| ESP-M35 | RGB LED center from PCB edge | ______ | mm | If enclosure visibility matters |
| ESP-M36 | Maximum LED/button protrusion above PCB | ______ | mm | |

## E. Pin Header Geometry

| ID | Measurement | Value | Unit | Notes |
|---|---|---:|---|---|
| ESP-M37 | Left header overall length | ______ | mm | Physical populated header |
| ESP-M38 | Right header overall length | ______ | mm | |
| ESP-M39 | Header pin pitch | ______ | mm | Measure only if physical verification is needed |
| ESP-M40 | Header height above PCB | ______ | mm | Important for case clearance |
| ESP-M41 | Header pin protrusion below PCB | ______ | mm | Important for mounting/support |
| ESP-M42 | Header row-to-row center distance | ______ | mm | Physical measurement |
| ESP-M43 | Header row to nearest PCB edge | ______ | mm | |

## F. Module / RF Clearance

These measurements are for enclosure design around the actual RF module and antenna region.

| ID | Measurement | Value | Unit | Notes |
|---|---|---:|---|---|
| ESP-M44 | Module shield/body maximum height above PCB | ______ | mm | Measure module body, not antenna keep-out |
| ESP-M45 | Module body length | ______ | mm | Physical module outline |
| ESP-M46 | Module body width | ______ | mm | Physical module outline |
| ESP-M47 | Antenna region start position from PCB edge | ______ | mm | Physical reference |
| ESP-M48 | Antenna region length | ______ | mm | Physical reference |
| ESP-M49 | Highest physical feature in antenna region | ______ | mm | Do not use this to define RF keep-out; use Espressif guidance for that |

## G. Case-Specific Measurements

Only measure these if the intended REAL Color Mate enclosure requires them.

| ID | Measurement | Value | Unit | Notes |
|---|---|---:|---|---|
| ESP-M50 | Required side-wall clearance for USB plug insertion | ______ | mm | Based on actual cable/plug to be used |
| ESP-M51 | Required clearance above PCB for case lid | ______ | mm | Based on highest component + design clearance |
| ESP-M52 | Required underside clearance | ______ | mm | Based on mounting/support concept |
| ESP-M53 | Required clearance around mounting screws/spacers | ______ | mm | Based on selected hardware |
| ESP-M54 | Interference distance to adjacent REAL Color Mate PCB | ______ | mm | Measure only after adjacent PCB geometry exists |

## H. Verification / Anomaly Record

| Item | Result |
|---|---|
| Physical board matches ESP32-S3 DevKitC-1 family | ______ |
| Purchased module marking matches ESP32-S3-WROOM-1 N16R8 | ______ |
| Board revision identified | ______ |
| Physical PCB outline agrees with Espressif drawing | ______ |
| Mounting holes agree with reference drawing | ______ |
| Connector locations agree with reference drawing | ______ |
| Any visible board modification or deviation | ______ |

## Measurement Rules

1. **Do not overwrite official Espressif reference values with measured values.** Keep reference and measured values separate.
2. Measurements in this file describe the purchased physical board only.
3. Do not infer hidden dimensions from photographs.
4. Do not use nominal component dimensions as substitutes for physical measurements when enclosure fit is involved.
5. If the physical board differs from the official drawing, record both values and the discrepancy.
6. Record the measurement tool and date when the measurements are entered.

## Reference Sources

- Espressif ESP32-S3-DevKitC-1 User Guide
- Espressif ESP32-S3-DevKitC-1 v1.0 User Guide
- Espressif ESP32-S3-DevKitC-1 v1.1 User Guide
- Espressif ESP32-S3-DevKitC-1 schematic
- Espressif ESP32-S3-DevKitC-1 PCB layout
- Espressif ESP32-S3-DevKitC-1 dimensions drawing / DXF
- Espressif ESP32-S3-DevKitC-1 v1.1 reference design

Official documentation confirms that board dimensions, PCB layout, schematic, dimensions drawing, DXF source, and reference design are available. citeturn0search0turn0search1turn0search6
