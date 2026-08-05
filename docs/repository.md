# Repository Structure

The repository layout is an operational (maintenance) reference and not part of the formal specification. This file is intended to document the current repository layout for contributors and maintainers.

```
REAL-Color-Mate/
├── hardware/          # KiCad PCB design
├── software/          # ESP32 firmware
├── mechanical/        # OpenSCAD / STEP / STL
├── calibration/       # Calibration data and procedures
├── docs/              # Design documents and research
├── manufacturing/     # Manufacturing instructions
├── tools/             # Development tools
├── BOM.md             # Bill of materials
├── MASTER_SPECIFICATION.md    # Official specifications (Single Source of Truth)
├── README.md          # Project overview
├── ROADMAP.md         # Development roadmap
├── IDEA.md            # Future ideas
├── CHANGELOG.md       # Version history
├── AGENTS.md          # AI collaboration rules and operational guidelines
└── .github/
    └── copilot-instructions.md # AI behavior rules
```

Notes:
- This file is intended for contributors and maintainers. It documents the current repository layout and may be updated as directory structure evolves.
- Repository layout is operational information and not a design specification. The authoritative specifications remain in MASTER_SPECIFICATION.md.
