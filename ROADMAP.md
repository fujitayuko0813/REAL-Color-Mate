# REAL Color Mate Roadmap

**Version:** 2.1  
**Last Updated:** 2026-08-26  
**Status:** Active Development

---

## Purpose

This document records planned development work for REAL Color Mate.

It is **not** a formal specification.

Formal requirements are defined only in [MASTER_SPECIFICATION.md](./MASTER_SPECIFICATION.md).

Design rationale is recorded in [docs/design_history.md](./docs/design_history.md).

Ideas and proposals that are not yet scheduled belong in [IDEA.md](./IDEA.md).

---

## Status Definitions

- **Complete** — verified as completed in the repository.
- **In Progress** — currently being worked on.
- **Next** — the next planned work item.
- **Planned** — scheduled future work.
- **Blocked** — cannot proceed until a prerequisite is resolved.
- **Unknown** — status cannot be verified from repository evidence.

---

## Phase 0 — Documentation Foundation

**Status: Complete**

- Establish `MASTER_SPECIFICATION.md` as the Single Source of Truth.
- Separate specifications from operational rules, design history, roadmap, and ideas.
- Establish `AGENTS.md` and `.github/copilot-instructions.md` rules.
- Establish `docs/design_history.md`.
- Establish `docs/component_selection.md`.
- Establish operational repository-layout documentation.

---

## Phase 1 — Component and Requirement Verification

**Status: Next**

- Verify the exact purchased ESP32-S3 DevKitC-1 N16R8 board dimensions.
- Verify the exact purchased AS7341 component/module documentation and channel definition.
- Measure the purchased MKS MINI12864 V3 mechanical dimensions.
- Verify the MKS MINI12864 V3 display-controller information.
- Determine the LED optical/mechanical placement distance during optical design.
- Resolve the battery, charger, and power-supply design requirements.
- Keep all unverified values as `Unknown` until verified.

Reference: [BOM.md](./BOM.md)

---

## Phase 2 — Optical Design

**Status: Planned**

- Develop the fixed 45° illumination / 0° observation geometry into a detailed optical design.
- Define the matte-black optical chamber implementation.
- Define the replaceable measurement hood.
- Verify LED placement and sensor geometry using measured component data.
- Document optical tolerances and verification procedures.

Prerequisite: Phase 1 component verification.

---

## Phase 3 — Electronics and PCB Design

**Status: Planned**

- Define the power system after the power requirements are verified.
- Design the custom PCB in KiCad.
- Integrate the selected MCU, AS7341, LED driver, display/UI, storage, and power circuitry.
- Verify electrical characteristics from authoritative component documentation.
- Produce manufacturing-ready PCB data after verification.

Prerequisite: Phase 1 and relevant Phase 2 information.

---

## Phase 4 — Mechanical Design

**Status: Planned**

- Design the portable enclosure in OpenSCAD.
- Integrate measured component dimensions.
- Design the optical chamber and replaceable measurement hood.
- Maintain serviceability and practical manufacturing clearances.
- Produce STEP/STL data after the design is verified.

Prerequisite: Verified component dimensions and optical design.

---

## Phase 5 — Firmware and Measurement Software

**Status: Planned**

- Implement the ESP32 Arduino Framework firmware.
- Implement spectral acquisition.
- Implement XYZ conversion.
- Implement CIE Lab conversion.
- Implement DeltaE calculation.
- Implement calibration handling.
- Implement CSV data logging.

Prerequisite: Verified hardware and measurement architecture.

---

## Phase 6 — Calibration and Validation

**Status: Planned**

- Establish the calibration procedure.
- Record calibration data separately from formal specifications.
- Verify measurement repeatability.
- Verify the complete optical/electronic measurement chain.
- Record measured results and limitations.

Prerequisite: Functional hardware and firmware.

---

## Phase 7 — Manufacturing Readiness

**Status: Planned**

- Finalize manufacturing documentation.
- Verify PCB manufacturing outputs.
- Verify mechanical manufacturing outputs.
- Consolidate BOM and procurement information.
- Perform final documentation consistency review.
- Mark production data only after required verification is complete.

Prerequisite: Successful validation.

---

## Roadmap Rules

- This file contains plans, not formal specifications.
- Do not treat a roadmap item as a decided requirement until it is explicitly approved and recorded in `MASTER_SPECIFICATION.md`.
- Do not invent completion status.
- If a prerequisite is unresolved, mark the item `Blocked` or `Unknown`.
- Approved changes to project requirements must be recorded in `CHANGELOG.md`.
