# REAL Color Mate — Optical Specification (v0.3-prelim)

Version: v0.3-prelim  
Status: Preliminary Design (Concept / Draft)

Purpose
-------
Define the optical design requirements and high-level implementation details for the REAL Color Mate v0.3 optical subsystem. This document covers the measurement geometry, selected components, primary optical requirements, mechanical constraints relevant to optics, stray-light countermeasures, and the calibration approach. This is a preliminary document: where values are not yet decided they are marked TBD or Unknown.

Optical Principle
-----------------
- Measurement geometry: 45° illumination / 0° observation (45/0).
  - Illumination delivered at nominal 45° to the local sample surface normal.
  - Detection (reception) is at 0° relative to the sample normal (perpendicular).
- Rationale: minimizes specular highlight contributions for diffuse-dominant automotive paints while providing repeatable geometry for colorimetric measurement and comparison against paint references.
- Measurement assumes a flat local sample region (or locally flattened area with measurement hood).

Components
----------
- Color sensor:
  - Adafruit AS7341 (11 spectral channels). Status: Decided.
- Illumination:
  - LED: Cree XP‑G4, 5000 K, CRI ≥ 90, arranged in an 8‑LED ring. Status: Decided.
  - LED ring driver and current control: TBD (electrical design to follow in later phase).
- Optomechanics:
  - Measurement hood (replaceable). Status: Decided.
  - Measurement aperture (defines measurement area). Size: TBD.
  - Internal chamber finish: matte (non-reflective) black. Status: Decided.
- Misc:
  - Light baffles / stray-light traps: Conceptual, details TBD.

Optical Requirements
--------------------
- Geometry:
  - Illumination angle: 45° nominal (relative to local surface normal). Tolerance: TBD.
  - Observation angle: 0° nominal (sensor optical axis normal to sample). Tolerance: TBD.
- Spectral response:
  - Native sensor channels: use AS7341 spectral bands. Mapping to standard colorimetric spaces (XYZ, Lab) is out of scope here (handled later by color science algorithms).
- Illumination:
  - Spectral target: approx. D50/D65 neighborhood (device LED chosen is 5000 K; exact spectrum will be measured and recorded).
  - Uniformity: Illuminance across measurement spot should be sufficiently uniform to meet repeatability targets. Specific uniformity target: TBD.
- Repeatability & Stability:
  - Measurement repeatability target: TBD (to be defined by test protocol).
  - Temperature dependence: Unknown; to be characterized in prototype stage.
- Measurement area:
  - Aperture size / effective measurement diameter: TBD. (Do NOT assume a value; measure and record in production design.)
- Ambient light rejection:
  - Device shall minimize ambient-light influence through mechanical design and processing (see Stray Light Countermeasures).

Mechanical Constraints
----------------------
- Case interior finish: matte black (to reduce internal reflections).
- Replaceable measurement hood:
  - Capture and reference alignment features to ensure consistent geometry.
  - Hood must allow flush contact or a controlled stand-off from measured surface; stand-off distance: TBD.
- Measurement aperture and hood must be serviceable and replaceable without changing core optical alignment.
- Tolerances and final mechanical dimensions are not decided at this stage — see OPTICAL_TOLERANCE.md.

Optical Layout
--------------
- A conceptual layout diagram is provided in OPTICAL_LAYOUT.svg (docs/optical/OPTICAL_LAYOUT.svg).
- Main elements shown:
  - LED ring concentric around measurement axis.
  - AS7341 sensor mounted approximately on the central axis to sample reflected light at 0°.
  - Measurement plane (sample surface) and measurement aperture.
  - 45° illumination rays intersecting the sample region outside the sensor axis.
- Exact sensor placement, lensing (if any), and mechanical offsets are TBD and must be confirmed during prototyping.

Stray Light Countermeasures
---------------------------
- Interior surfaces: matte black, low reflectance paint/materials.
- Baffles:
  - Use stepped internal baffles between LEDs and sensor to prevent direct LED scatter into the sensor.
- Light traps:
  - Geometry that absorbs off-axis reflections within the hood.
- Aperture:
  - Use a well-defined measurement aperture to limit field-of-view to the intended sample area.
- Seal / shrouding:
  - Hood seals to sample surface to minimize ambient ingress when practical (design for both contact and non-contact measurements).
- Material selection and surface finish to be validated in prototype; for all uncertain choices mark status as TBD/Unknown.

Calibration
-----------
- High-level calibration steps are described in docs/optical/CALIBRATION.md.
- Only white and black (dark) calibrations are required at this stage (device-level radiometric offsets and scaling). Colorimetric transformation algorithms are out of scope for this document.
- Calibration files, formats, and storage locations: TBD.

Future Improvements
-------------------
- Consider narrow-band or filtered illuminants to better match colorimetric transformations.
- Investigate adding diffuser/lens to improve illumination uniformity.
- Characterize LED spectral variation and incorporate temperature compensation.
- Define measurement spot sizes (small/large hoods) for different paint surface conditions.

References
----------
- MASTER_SPECIFICATION.md — project authority (Single Source of Truth).  
- Adafruit AS7341 product documentation / datasheet. (Link to datasheet: TODO/Unknown — include official link in production document.)  
- Cree XP‑G4 datasheet (LED spectral and thermal characteristics): link TBD.  
- Standard color measurement geometry references (45/0 geometry notes): link TBD.

Notes and Warnings
------------------
- Do NOT invent final dimensions, tolerances, or calibration constants. Where parameters are not yet decided, the terms "TBD" or "Unknown" are used.
- This document covers only optical-design-level decisions. PCB and electronic details are deferred until the optical geometry is locked.
