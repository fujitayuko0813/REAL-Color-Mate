# REAL Color Mate - BOM
Version: 0.3.0
Last Updated: 2026-08-01
Status: Concept Design

---

# Bill of Materials (BOM)

## Core Hardware

| Ref | Part | Manufacturer | Part Number | Qty | Status | Notes |
|------|------|--------------|-------------|----:|--------|-------|
| MCU-01 | ESP32-S3 DevKitC-1 N16R8 | Espressif | ESP32-S3-WROOM-1 N16R8 | 1 | Purchased | Main MCU |
| SEN-01 | Spectral Sensor | Adafruit | AS7341 | 1 | Purchased | 10-channel spectral sensor |
| LED-01 | White LED | Cree LED | XPGEWT-02-0000-00000UHE3 | 12 | Purchased | Use 8, keep 4 as spare |
| DRV-01 | LED Driver | STMicroelectronics | ALED8102SXTTR | 2 | Purchased | Use 1, keep 1 as spare |
| LCD-01 | LCD Module | Makerbase | MKS MINI12864 V3 | 1 | Purchased | ST7567 LCD + Encoder + microSD + Buzzer |

---

# Optical System

| Item | Specification | Status |
|------|---------------|--------|
| Illumination | 45° Ring Illumination | Fixed |
| Receiver | 0° Sensor | Fixed |
| LEDs Used | 8 LEDs | Fixed |
| Spare LEDs | 4 LEDs | Fixed |

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
| ESP32-S3 | Planned |
| CIE Lab | Planned |
| DeltaE76 | Planned |
| DeltaE94 | Planned |
| DeltaE2000 | Planned |
| CSV Logging | Planned |

---

# Development Notes

Confirmed Design Rules

- ESP32-S3 is the main MCU.
- AS7341 is the only spectral sensor.
- Cree XP-G4 LEDs are fixed.
- Eight LEDs are used.
- Four LEDs remain as spare.
- ALED8102SXTTR drives the LEDs.
- MKS MINI12864 V3 is used for UI.
- Measurement geometry is fixed at 45° / 0°.
- Arduino IDE is used.
- Concept Design and Production Design must be managed separately.

---

# Change History

## v0.3.0

- Updated MCU to ESP32-S3 DevKitC-1 N16R8
- Added purchased hardware
- Updated LCD module
- Updated LED quantity
- Added Development Notes
