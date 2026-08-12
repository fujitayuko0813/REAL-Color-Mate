# OPTICAL_TOLERANCE.md

Version: v0.3-prelim

Status: Preliminary — Tolerances are not finalized. Numeric tolerances intentionally left as TBD unless explicitly measured and verified.

Purpose
- Describe critical tolerance classes and how they affect measurement performance.
- Provide guidance for later tolerance allocation during detailed design and verification.

General guidance
- Do not assume any numeric tolerance values from this document. All numeric tolerances must be determined by optical analysis, mechanical constraints, and verification testing.
- Keep design for manufacturability in mind: prefer common machining tolerances where possible and apply tighter tolerances only to features that directly affect optical performance.

Critical tolerance areas (descriptions only)
1. Optical axis alignment
   - Description: Angular and lateral alignment between illuminator, diffuser, lens optical axis, and sensor centerline.
   - Effect: Misalignment causes non-uniform illumination, vignetting, and color measurement errors.
   - Value: TBD

2. Working distance
   - Description: Distance from sample surface to lens entrance pupil.
   - Effect: Focus, field-of-view, and sampling footprint depend on working distance.
   - Value: TBD

3. Aperture and stop location
   - Description: Position and size of aperture stop relative to lens elements.
   - Effect: Depth-of-field, stray light, and illumination fall-off.
   - Value: TBD

4. Surface flatness and parallelism (sample interface)
   - Description: Flatness of sample support plane and parallelism to optical axis.
   - Effect: Focus uniformity across measurement area.
   - Value: TBD

5. Mechanical fastener and mounting features
   - Description: Repeatable mount datums for lenses, sensor board, and LEDs.
   - Effect: Instrument-to-instrument reproducibility.
   - Value: TBD

6. Stray light baffling and internal surface finishes
   - Description: Reflectivity of internal surfaces and baffle positions.
   - Effect: Signal-to-noise and ghost reflections that bias color readings.
   - Value: TBD

Verification and test
- During prototype build, measure sensitivity of color readings to controlled perturbations in each critical area above.
- Generate a tolerance allocation table after empirical sensitivity data is available.

Notes
- Preserve TBD/Unknown where data is not available.
- Final tolerances must be recorded in the MASTER_SPECIFICATION.md only after approval.

