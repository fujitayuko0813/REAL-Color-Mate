# CHANGELOG

All notable changes for REAL Color Mate.

---

## [2.1] - 2026-08-19

### Specification Synchronization

#### Changed

- **MASTER_SPECIFICATION.md** updated to v2.1.
- Approved **ESP32-S3 DevKitC-1 N16R8** as the main MCU, synchronized with the purchased BOM.
- Normalized the selected Cree XP-G4 and ALED8102SXTTR part information.
- Removed the previously recorded AS7341 channel count because it was not sufficiently verified in the repository and replaced it with `Unknown` pending verification.
- Added the selected MKS MINI12864 V3 display/UI module to the hardware specification.
- **BOM.md** updated to v1.0.0 and synchronized with MASTER_SPECIFICATION v2.1.
- Added an explicit verification list for dimensions, power system, optical placement, and other values that must not be guessed.

#### Reason

The repository contained a material inconsistency between MASTER_SPECIFICATION.md and BOM.md, most importantly the MCU selection. The purchased BOM already specified ESP32-S3 DevKitC-1 N16R8, while the master specification still listed ESP32-WROOM-32. The project owner explicitly approved the ESP32-S3 selection on 2026-08-19.

#### Verification Policy

Unknown or unverified values remain explicitly marked `Unknown`. No physical dimensions, calibration values, electrical characteristics, or performance specifications were invented during this synchronization.

---

## [2.0] - 2026-08-04

### Documentation Refactoring (No Specification Changes)

#### Changed

- **AGENTS.md**: Refactored to remove duplicated technical specifications
  - Replaced technical specifications with references to MASTER_SPECIFICATION.md
  - Reorganized file structure for clarity
  - Kept only operational guidance and AI collaboration rules
  - Status: Specifications preserved, operational guidance clarified

- **.github/copilot-instructions.md**: Updated reading order and references
  - Changed reading order to: MASTER_SPECIFICATION.md → CHANGELOG.md → AGENTS.md
  - Added "Single Source of Truth" emphasis for MASTER_SPECIFICATION.md
  - Updated all specification references to point to MASTER_SPECIFICATION.md
  - Version bumped to 2.0
  - Status: Reading order clarified, references verified

#### Verified

- MASTER_SPECIFICATION.md remains unchanged (Single Source of Truth)
- All project specifications preserved
- No hardware specifications modified
- No software specifications modified
- No optical specifications modified
- No calibration specifications modified
- Documentation is internally consistent
- No broken internal links
- Repository structure unchanged

### Rationale

This refactoring improves separation of responsibilities:
- MASTER_SPECIFICATION.md: Official specifications (authority)
- AGENTS.md: Operational guidance and AI collaboration rules
- .github/copilot-instructions.md: Copilot-specific workflow instructions

The refactoring maintains all project decisions while clarifying documentation structure.

---
