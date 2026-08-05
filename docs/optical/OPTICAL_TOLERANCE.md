# Optical Tolerance Specification (Preliminary Design)

Version: v0.3-prelim  
Status: Preliminary Design — Draft

This file captures preliminary tolerance items for the optical design. Many dimensions and tolerances are not yet decided; therefore this document is managed as a "Preliminary Design" and each entry is marked with Status = Draft. Do not treat any numeric tolerance here as production-ready.

General instructions
--------------------
- Stage: Preliminary (Concept / Draft)
- Document role: track which optical dimensions/tolerances need specification in the production design stage.
- Where values are not decided, entries show "TBD" or "Unknown".
- During prototype iteration, measure actual dimensions and update these tolerances into Production Design.

Tolerance items
---------------
1. LED ring concentricity
   - Description: concentric alignment of LED ring to measurement axis.
   - Required tolerance: TBD
   - Verification method: optical alignment jig / camera inspection.
   - Status: Draft

2. Illumination angle (nominal 45°)
   - Description: angular deviation of illumination relative to sample normal.
   - Tolerance (angular): TBD
   - Verification method: mechanical protractor jig or optical measurement.
   - Status: Draft

3. Observation axis alignment (0°)
   - Description: angular and lateral alignment of sensor optical axis to measurement center.
   - Angular tolerance: TBD
   - Lateral offset tolerance: TBD
   - Verification method: mechanical datum and alignment fixture.
   - Status: Draft

4. Aperture diameter and edge quality
   - Description: effective measurement aperture diameter and edge rounding.
   - Value: TBD
   - Geometric tolerance: TBD
   - Verification method: optical measurement of spot size and illumination footprint.
   - Status: Draft

5. Sensor-to-aperture distance
   - Description: distance from AS7341 active area (or aperture plane) to sample plane.
   - Value: TBD
   - Tolerance: TBD
   - Verification method: mechanical gauge / optical focus test.
   - Status: Draft

6. Hood seal and stand-off
   - Description: hood-to-sample interface geometry for contact and non-contact modes.
   - Stand-off distance: TBD
   - Repeatability: TBD
   - Verification method: mechanical gauge, repeatability test on sample surfaces.
   - Status: Draft

7. Internal baffle positioning
   - Description: location and angle of internal baffles/traps.
   - Position tolerance: TBD
   - Verification method: light leak tests and stray-light measurement.
   - Status: Draft

8. Manufacturing allowances
   - Description: tolerances accounting for 3D printing/assembly variability.
   - Allowances: TBD (dependent on chosen manufacturing process).
   - Status: Draft

Notes & next steps
------------------
- Convert the most critical items (illumination angle tolerance, observation axis alignment, aperture diameter, and sensor-to-aperture distance) from TBD to decided values during prototype build and metrology.
- For each item moved from Draft to Production, include exact numeric tolerances, inspection procedures, and acceptance criteria.
- If any parameter cannot be measured sufficiently, mark as Unknown and define a test plan to determine the required tolerance.
