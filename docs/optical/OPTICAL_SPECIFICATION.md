# OPTICAL_SPECIFICATION.md

Version: v0.3-prelim
Document: Preliminary Optical Design for REAL Color Mate v2.0

Status: Preliminary Design — DO NOT FINALIZE. This document is part of the REAL Color Mate v2.0 optical design (v0.3-prelim). It is intended to record design intent, constraints, and open items. Any numeric value left unknown is marked as "TBD" or "Unknown" and must not be assumed or reified without explicit verification and approval.

References
- MASTER_SPECIFICATION.md (Single Source of Truth) — DO NOT MODIFY
- docs/optical/OPTICAL_LAYOUT.svg
- docs/optical/OPTICAL_TOLERANCE.md
- docs/optical/CALIBRATION.md

Scope
- Defines the optical subsystem scope for REAL Color Mate v2.0 (v0.3-prelim).
- Covers illumination, collection optics, sensor interface, and calibration strategy at a preliminary level.

Design Goals
- Portable color measurement tool suitable for automotive paint matching.
- Repeatable, traceable color measurements under controlled illumination.
- Compact, manufacturable optical layout compatible with enclosure constraints (see MASTER_SPECIFICATION.md for mechanical constraints).

Overall Architecture
- Illumination subsystem: integrated multi-channel LED source with diffuser and geometry to provide near-Lambertian field. (Detailed LED model and spectral power distributions: TBD)
- Collection optics: lens or lens group to image the sample area onto the color sensor with controlled field-of-view and minimal stray light. (Lens prescription: TBD)
- Sensor: color image sensor / colorimeter module interfacing with ESP32 firmware. Exact sensor part number and spectral responsivity: TBD.
- Aperture and baffling: internal aperture, baffles, and stray-light control implemented in mechanical housing. Exact positions and dimensions: TBD.

Key Requirements (Preliminary)
- Measurement area (sample footprint): TBD
- Working distance (sample surface to lens entrance): TBD
- Illumination uniformity across measurement area: Target — high uniformity; numeric target: TBD
- Spectral channels: Candidate approach — broad-spectrum white LED + narrowband/filtered channels or RGB LED array; final choice: TBD
- Measurement repeatability (instrument-to-self): TBD
- Target device operating temperature range: refer to MASTER_SPECIFICATION.md

Open Items / TBD (do NOT invent values)
- Exact LED models and spectral power distributions — TBD
- Lens prescription, focal length, and numerical aperture — TBD
- Sensor model and spectral responsivity curves — TBD
- Mechanical mounting positions and fastener details for optics — TBD
- Absolute calibration coefficients and per-device lookup tables — TBD

Safety and Compliance
- Ensure LED drive currents and thermal designs conform to electrical and thermal limits in MASTER_SPECIFICATION.md and BOM.md.

Traceability and Versioning
- This document is v0.3-prelim and is preliminary. When items are finalized they must be recorded in MASTER_SPECIFICATION.md per project rules.

Notes
- Do not change MASTER_SPECIFICATION.md, CHANGELOG.md, AGENTS.md, or other existing files as part of this change.
- This commit introduces only the files listed in the accompanying commit metadata.

