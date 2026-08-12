# CALIBRATION.md

Version: v0.3-prelim

Status: Preliminary — calibration procedure draft. Do not record or bake numeric calibration coefficients into this file. All device-specific calibration data must be stored in the calibration/ directory as per project rules and in device-specific artifacts.

Purpose
- Describe the intended calibration workflow for the optical subsystem of REAL Color Mate v2.0.
- Provide a reproducible procedure to create calibration artifacts and to perform per-unit calibration without inventing final calibration coefficients.

Calibration strategy (conceptual)
- Radiometric calibration: map raw sensor digital counts to relative radiometric units using uniform reference targets and controlled illumination. Absolute radiometry (W/sr/m^2/nm) is outside the scope of this preliminary design unless a NIST-traceable light source and spectroradiometer are used.
- Colorimetric calibration: derive device-specific transforms from sensor channels to standard color spaces (e.g., CIE XYZ or CIELAB) using a set of reference patches with known colorimetric values. Reference values may be obtained from calibrated color tiles or a reference spectrophotometer. Specific transforms and coefficients: TBD.

Suggested calibration artifacts (examples — choose available, traceable artifacts)
- White reference tile (highly reflective, near-Lambertian). Part/model: TBD.
- Neutral gray tiles spanning measurement range (e.g., 90%, 50%, 10% reflectance) — model: TBD.
- Color reference card or full color chart with known XYZ/CIELAB values — model: TBD.

Procedure (high level)
1. Warm-up
   - Power device and allow illumination system to reach steady-state thermal condition. Warm-up time: TBD (measure during verification).
2. Dark measurement
   - With illumination off (or light path blocked), record dark frames for noise and offset estimation. Capture multiple frames and compute mean dark offset per channel.
3. White reference
   - Place white reference tile at sample position. Capture multiple frames under nominal illumination settings. Compute mean response and normalize per-channel gains.
4. Gray steps (optional)
   - Capture neutral gray tiles to check linearity and exposure response.
5. Color reference
   - Capture color chart patches. Using known reference XYZ/CIELAB values (from a calibrated spectrophotometer or manufacturer data), compute the color transform (e.g., 3x3 matrix + offset, or higher-order polynomial) from sensor RGB to target color space. Coefficients: TBD and must be saved per unit.
6. Verification
   - Re-measure a held-out set of patches and compute color difference metrics (e.g., ΔE*ab or ΔE2000). Target acceptance criteria: TBD.
7. Storage
   - Save calibration coefficients, metadata (illumination current, temperature, serial number), and raw captures in the calibration/ directory for traceability. Do NOT hard-code numeric coefficients into firmware without a clear versioning and update mechanism.

Software notes
- Provide a calibration utility (desktop or CLI) to run the above procedure and produce calibration artifacts. Implementation details and scripts: TBD and should be added to tools/ or software/ when available.

Uncertainty and Traceability
- Document measurement uncertainty and test equipment used. If absolute calibration is required, include NIST-traceable instrumentation in the calibration chain.

Notes
- This file intentionally does not contain finalized numeric calibration coefficients.
- Keep values marked TBD until verified by measurement.

