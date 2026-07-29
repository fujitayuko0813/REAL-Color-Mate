# REAL Color Mate - AI Development Guide

## Project

Portable Color Measurement Tool for Automotive Paint Matching

This project is intended to assist automotive paint color matching.
It is NOT intended to replicate commercial color matching systems.

## Goals

- Measure spectral data
- Convert to XYZ
- Convert to CIE Lab
- Calculate DeltaE76
- Calculate DeltaE94
- Calculate DeltaE2000
- Save CSV
- Support calibration
- Generate manufacturing data

## Development Rules

- Do not guess specifications.
- If unknown, clearly state "Unknown".
- Separate Concept Design and Production Design.
- Always include version numbers.
- Always include change history.
- Maintain consistency between PCB, Case, BOM and Software.
- Use purchasable components.

## Hardware

ESP32-WROOM-32

AS7341

Cree XP-G4

ALED8102

5V System

## Software

Arduino IDE

ESP32

KiCad

OpenSCAD

CSV

## Output

Every task must produce actual files whenever possible.
