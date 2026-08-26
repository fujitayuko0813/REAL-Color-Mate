# CHANGELOG

All notable changes for REAL Color Mate.

---

## [2.1] - 2026-08-26

### Documentation Structure Synchronization

#### Changed

- Completed `docs/component_selection.md` as the component-selection history and verification record.
- Added explicit `Selected`, `Purchased`, `Candidate`, `Rejected`, and `Unknown` status definitions to the component-selection document.
- Recorded currently verifiable component-selection information without inventing missing rationale, prices, availability, dimensions, or specifications.
- Updated `AGENTS.md` to Version 2.1 and aligned its operating rules with the current v2.1 specification.
- Updated `.github/copilot-instructions.md` to Version 2.1 and removed stale references to sections that no longer exist in `MASTER_SPECIFICATION.md`.
- Moved repository-structure guidance out of the formal specification and into operational documentation.
- Confirmed `docs/repository.md` as the operational repository-layout reference.
- Expanded `ROADMAP.md` into a staged development plan based on the currently documented requirements, BOM, and verification items.
- Expanded `IDEA.md` into a controlled idea/proposal register without inventing historical ideas.
- Finalized `README.md` as the project navigation entry point.
- Added `docs/README.md` as the documentation index.

#### Reason

The v2.1 documentation structure had stale cross-references and overlapping responsibilities. The roadmap and idea documents were also only placeholders, which made the next development step unclear. The documentation has now been organized so that formal requirements, operational rules, plans, ideas, design rationale, component selection, and repository navigation have distinct responsibilities.

#### Verification Policy

Unknown or unverified values remain explicitly marked `Unknown`. No physical dimensions, calibration values, electrical characteristics, or component performance specifications were invented during this documentation synchronization.

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

- **AGENTS.md**: Refactored to remove duplicated technical specifications.
- **.github/copilot-instructions.md**: Updated reading order and references.
- Established `MASTER_SPECIFICATION.md` as the Single Source of Truth.
- Separated operational guidance from formal specifications.

#### Verified

- Project specifications were preserved.
- No hardware specifications were modified.
- No software specifications were modified.
- No optical specifications were modified.
- No calibration specifications were modified.

### Rationale

This refactoring established the documentation separation used by Version 2.x:

- `MASTER_SPECIFICATION.md`: Official specifications
- `AGENTS.md`: Operational guidance and AI collaboration rules
- `.github/copilot-instructions.md`: Copilot-specific workflow instructions
- `CHANGELOG.md`: Approved change history
- `ROADMAP.md`: Planned development work
- `IDEA.md`: Future ideas and proposals
- `docs/design_history.md`: Design rationale and decision history
- `docs/component_selection.md`: Component selection history and verification
