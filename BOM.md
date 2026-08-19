# REAL Color Mate - BOM
Version: 1.0.0
Last Updated: 2026-08-19
Status: Concept Design

---

# Bill of Materials (BOM)

## Core Hardware

| Ref | Part | Manufacturer | Part Number | Qty | Status | Notes |
|------|------|--------------|-------------|----:|--------|-------|
| MCU-01 | ESP32-S3 DevKitC-1 N16R8 | Espressif | ESP32-S3-WROOM-1 N16R8 | 1 | Purchased | Main MCU |
| SEN-01 | Spectral Sensor | Adafruit | AS7341 | 1 | Purchased | Spectral sensor; channel definition: Unknown until verified |
| LED-01 | White LED | Cree LED | XPGEWT-02-0000-00000UHE3 | 12 | Purchased | Use 8, keep 4 as spare |
| DRV-01 | LED Driver | STMicroelectronics | ALED8102SXTTR | 2 | Purchased | Use 1, keep 1 as spare |
| LCD-01 | LCD Module | Makerbase | MKS MINI12864 V3 | 1 | Purchased | Display and user interface module |

---

# Optical System

| Item | Specification | Status |
|------|---------------|--------|
| Illumination | 45° Ring Illumination | Fixed |
| Receiver | 0° Sensor | Fixed |
| LEDs Used | 8 LEDs | Fixed |
| Spare LEDs | 4 LEDs | Fixed |
| Optical Chamber | Matte black | Fixed |
| Measurement Hood | Replaceable | Fixed |

---

# Power System

| Ref | Part | Status |
|------|------|--------|
| BAT-01 | Battery | Not Purchased |
| CHG-01 | Battery Charger Circuit | Not Purchased |
| PWR-01 | Power Supply Circuit | Not Purchased |

---

# PCB

| Item | Status |
|------|--------|
| Custom PCB | Not Designed |
| KiCad Project | Not Started |
| Gerber | Not Generated |

---

# Enclosure

| Item | Status |
|------|--------|
| 3D Printed Case | Not Designed |
| Optical Hood | Not Designed |
| Diffuser | Not Purchased |
| Light Shield | Not Purchased |

---

# Software

| Item | Status |
|------|--------|
| Arduino IDE | Planned |
| ESP32-S3 Arduino Framework | Planned |
| Spectral acquisition | Planned |
| XYZ conversion | Planned |
| CIE Lab | Planned |
| DeltaE | Planned |
| Calibration | Planned |
| CSV Logging | Planned |

---

# Confirmed Design Rules

- ESP32-S3 DevKitC-1 N16R8 is the main MCU.
- AS7341 is the selected spectral sensor.
- Cree XP-G4 LEDs are fixed.
- Eight LEDs are used; four remain as spare.
- ALED8102SXTTR is the selected LED driver.
- MKS MINI12864 V3 is the selected display/UI module.
- Measurement geometry is fixed at 45° / 0°.
- Arduino IDE and ESP32 Arduino Framework are used.
- Concept Design and Production Design must be managed separately.
- Dimensions, electrical characteristics, calibration values, and performance specifications must not be guessed. Use `Unknown` until verified.

---

# Verification Items

| Item | Status | Required Action |
|------|--------|-----------------|
| ESP32-S3 exact board dimensions | Unknown | Measure purchased board |
| AS7341 exact channel definition | Unknown | Verify exact sensor/module documentation |
| MKS MINI12864 V3 mechanical dimensions | Unknown | Measure purchased module |
| LED optical/mechanical placement distance | Unknown | Determine during optical design and verification |
| Battery selection | Unknown | Decide after power budget |
| Charger circuit | Unknown | Decide after battery selection |
| Power supply circuit | Unknown | Design after power budget |
| PCB dimensions | Unknown | Determine during PCB design |
| Case dimensions | Unknown | Determine after actual component measurements |

---

# Development Status

### Purchased
- MCU-01
- SEN-01
- LED-01
- DRV-01
- LCD-01

### Not Yet Designed
- Custom PCB
- KiCad project
- Production case
- Optical hood
- Power system
- Firmware
- Calibration system

---

# Change History

## v1.0.0 — 2026-08-19

- Synchronized BOM with approved MASTER_SPECIFICATION v2.1.
- Confirmed ESP32-S3 DevKitC-1 N16R8 as the main MCU.
- Normalized LED and driver part numbers to the purchased BOM.
- Removed unverified AS7341 channel count.
- Added explicit verification items and Unknown status where information is not yet verified.
