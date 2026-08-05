# Calibration Procedure — Optical Subsystem (v0.3-prelim)

Version: v0.3-prelim  
Status: Preliminary Design — Draft

Scope
-----
This document covers the basic radiometric calibration procedures required at the current stage: white calibration and black (dark) calibration. Colorimetric transformations (XYZ, Lab, DeltaE) and spectral-to-color conversions are out of scope for this document and will be defined later.

General notes
-------------
- Perform calibrations in a stable environment (controlled ambient light if possible).
- Record calibration metadata: date/time, device serial, LED drive current, ambient temperature, firmware version, and any hood used.
- Calibration file format and storage (file name, JSON/CSV schema) are TBD and will be defined in the production documentation.

White Calibration (Reference)
------------------------------
Purpose: establish scale factors or reference response for each sensor channel to map measured signals to a reference whitened reflectance.

Equipment:
- Diffuse white reference tile or panel with known high reflectance (e.g., Spectralon or certified white tile). If a certified tile is not available, note that calibration quality will be limited.
- Stable mount or fixture to hold tile perpendicular to measurement axis or in a repeatable geometry.

Procedure (high-level):
1. Ensure device is warmed up to operating conditions (LEDs and sensor have reached stable temperature). Warm-up time: TBD.
2. Mount the white reference in the measurement position / place the hood over the reference to replicate normal measurement geometry.
3. Disable external ambient light or minimize it (use dark room or shroud).
4. Set LED drive/current to the nominal calibration value used in measurement. Record LED settings.
5. Take N measurements (N ≥ 3 recommended) and average the raw channel readings to reduce noise.
6. Save the averaged channel readings as the "white reference" record.
7. Optionally, measure at multiple brightness levels if dynamic range scaling is required.
8. Mark file: calibration type = white, sample = reference_tile, date/time, device serial, LED settings.

Notes:
- If a certified spectral reflectance is available, store the spectral reference alongside device readings for future spectral calibration.
- If the white reference is variable (non-certified), mark status and include reference id.

Black (Dark) Calibration
------------------------
Purpose: measure dark offsets, bias, and sensor dark current to subtract from subsequent measurements.

Equipment:
- Opaque shutter/cover that prevents any light reaching the sensor while preserving the device arrangement (or fully turn off LEDs and cover aperture).
- Alternatively, perform dark measurement with LEDs off and hood closed.

Procedure:
1. With the device in measurement configuration, place the opaque shutter/cover over the aperture (or close the hood) to block incoming light.
2. Ensure LEDs are turned off (or set to calibration dark state) if required by the measurement method.
3. Take N measurements (N ≥ 3 recommended) and average to obtain channel dark offsets.
4. Save averaged values as "black" or "dark" reference (metadata: date/time, device serial, temperature, LED state).

Applying calibrations
---------------------
- For each raw measurement, subtract the saved dark offsets (black calibration) from raw channel readings.
- Optionally, divide by the white reference (after dark subtraction) to produce a relative reflectance vector (per-channel normalized signal).
- The exact transformation chain (raw → dark-corrected → white-normalized → colorimetric conversion) will be defined when color science algorithms are implemented.

Verification & validation
-------------------------
- After performing white and black calibrations, verify by measuring the white reference again and confirming the normalized response is within expected stability bounds (bounds TBD).
- Track calibration drift across time and temperature; define recalibration interval in production.

Storage & format
----------------
- Calibration file naming, format, and storage path: TBD.
- Recommended to use a small structured format (JSON or CSV with metadata) that includes:
  - device_id / serial
  - calibration_type (white / black)
  - timestamp
  - LED settings
  - averaged_channel_values (array)
  - temperature (if available)
  - hood_id (if applicable)
  - operator (optional)

Limitations
-----------
- This stage does not define spectral-to-colorimetric conversion coefficients.
- Calibration quality depends strongly on the quality of the white reference tile; use certified reference for production-level accuracy.
