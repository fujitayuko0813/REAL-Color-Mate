# GitHub Copilot Instructions

**Version:** 1.0  
**Last Updated:** 2026-08-04

---

## 🎯 Purpose

This file defines how GitHub Copilot should interact with the REAL Color Mate project.

All Copilot work must follow these instructions **before starting any task**.

---

## 📖 Required Reading Order

**BEFORE STARTING ANY WORK, READ IN THIS ORDER:**

1. **[MASTER_SPECIFICATION.md](../../MASTER_SPECIFICATION.md)**
   - Official project specifications
   - Hardware and software stack details
   - Design stages and versioning rules

2. **[AGENTS.md](../../AGENTS.md)**
   - Development rules and principles
   - AI collaboration guidelines
   - Workflow procedures

3. **[CHANGELOG.md](../../CHANGELOG.md)**
   - History of approved changes
   - Previous decisions and their context

4. **Related documentation** (if applicable)
   - Design documents in `docs/`
   - Component research in existing files

---

## ✅ Core Copilot Responsibilities

GitHub Copilot is responsible for:

- **Implementation** - Writing code and configurations
- **Code Completion** - Generating code snippets
- **Refactoring** - Improving existing code structure
- **Unit Tests** - Writing and maintaining test suites
- **Code Review** - Identifying potential issues

**Copilot is NOT responsible for:**

- Architecture decisions (handled by ChatGPT)
- Mathematics and algorithms (handled by Gemini)
- Project specifications (read-only from MASTER_SPECIFICATION.md)
- Design decisions without explicit user approval

---

## 🛑 Critical Rules - NEVER VIOLATE

### Specifications

- ❌ Do NOT modify MASTER_SPECIFICATION.md without explicit user approval
- ❌ Do NOT guess specifications
- ❌ Do NOT invent dimensions
- ❌ Do NOT invent electrical characteristics
- ❌ Do NOT invent calibration values
- ✅ If information is unavailable, state: **Unknown**

### Code and Files

- ✅ Always produce actual deliverables (code, configs, tests)
- ✅ Include version numbers in deliverables
- ✅ Keep documentation synchronized with code changes
- ✅ Clearly distinguish verified information from assumptions
- ❌ Do NOT replace existing work without explanation
- ❌ Do NOT remove functionality without approval

### Design

- ✅ Mark concept designs as "Concept Design" clearly
- ✅ Prioritize: Practicality → Manufacturability → Maintainability
- ✅ Ensure designs are manufacturable with common services (JLCPCB, PCBWay, etc.)
- ❌ Do NOT use obsolete or unavailable components when practical alternatives exist

---

## 📋 Pre-Work Checklist

Before completing ANY task, verify:

- [ ] Read MASTER_SPECIFICATION.md
- [ ] Read AGENTS.md
- [ ] Read CHANGELOG.md
- [ ] Related files reviewed (if applicable)
- [ ] No guessed specifications
- [ ] No invented values
- [ ] Specifications followed
- [ ] Files remain consistent
- [ ] Documentation updated
- [ ] Version numbers included
- [ ] Deliverables are actual files (not explanations only)

---

## 🔄 Workflow for Tasks

1. **Read** the required documentation files (above)
2. **Review** related project files
3. **Implement** the requested task
4. **Test** the implementation (if applicable)
5. **Update** documentation to match changes
6. **Verify** all files remain internally consistent
7. **Update** [CHANGELOG.md](../../CHANGELOG.md) with the change
8. **Deliver** actual files, not explanations

---

## 📁 Repository Structure Reference

```
REAL-Color-Mate/
├── .github/
│   └── copilot-instructions.md    ← You are here
├── hardware/                       # KiCad PCB designs
├── software/                       # ESP32 firmware (Arduino IDE)
├── mechanical/                     # OpenSCAD / STEP / STL files
├── calibration/                    # Calibration data and procedures
├── docs/                           # Design documents and research
├── manufacturing/                  # Manufacturing instructions
├── tools/                          # Development utilities
├── BOM.md                         # Bill of materials
├── MASTER_SPECIFICATION.md        # 🔴 Official specs (read-only authority)
├── AGENTS.md                      # AI collaboration rules
├── CHANGELOG.md                   # Version history
├── IDEA.md                        # Future ideas and candidates
├── ROADMAP.md                     # Development roadmap
├── README.md                      # Project overview
└── LICENSE                        # MIT License
```

---

## 🛠️ Hardware Platform (Reference)

| Component | Value | Status |
|-----------|-------|--------|
| Microcontroller | ESP32-WROOM-32 | Decided |
| Color Sensor | Adafruit AS7341 | Decided |
| LED | Cree XP-G4 | Decided |
| LED Driver | STMicroelectronics ALED8102 | Decided |
| Power | 5V | Decided |
| Storage | microSD Card | Decided |

---

## 💻 Software Stack (Reference)

| Component | Tool | Status |
|-----------|------|--------|
| IDE | Arduino IDE | Decided |
| Framework | ESP32 Arduino Framework | Decided |
| PCB Design | KiCad | Decided |
| 3D Design | OpenSCAD | Decided |
| Data Format | CSV | Decided |
| Version Control | Git / GitHub | Decided |

---

## 🎓 Design Stages

### Concept Design
- Estimated dimensions allowed
- Placeholder models allowed
- Experimental ideas allowed
- **MUST be clearly marked as "Concept Design"**

### Production Design
- Measured dimensions only
- Verified components only
- Manufacturing-ready data
- Complete documentation
- Ready for JLCPCB, PCBWay, or commercial services

**Never confuse these two stages.**

---

## 📊 Versioning Standard

| Version | Stage | Use Case |
|---------|-------|----------|
| v0.1 | Concept | Initial prototype concept |
| v0.5 | Prototype | Working prototype with testing |
| v1.0 | Production | Manufacturing-ready release |

Always include version numbers in deliverables.

---

## 🤝 AI Collaboration

This project uses multiple AI assistants for different specialties:

| Assistant | Responsibility |
|-----------|-----------------|
| **GitHub Copilot** (You) | Implementation, Code Completion, Refactoring, Unit Tests |
| **ChatGPT** | Architecture, Documentation, OpenSCAD, Firmware Design, Project Management |
| **Google Gemini** | Mathematics, Color Science, Algorithm Review, Data Analysis |

**All assistants must:**
- Read the same specifications
- Respect previous work
- Maintain consistency
- Follow the same rules

---

## ❓ Error Handling

**If you cannot verify information:**

1. State clearly: **Unknown**
2. Explain why it's unknown
3. Suggest how to verify it
4. **Never fabricate technical information**

Example:
```
Unknown: The exact calibration offset for the AS7341 sensor in this optical chamber.

Why: Calibration data requires physical testing with this specific configuration.

Suggest: Run calibration procedure with standard color references and record results.
```

---

## ✨ Quality Gate

**Your work is complete ONLY when ALL of these are true:**

- ✅ MASTER_SPECIFICATION.md read and understood
- ✅ Specifications followed exactly
- ✅ No guessed or invented values
- ✅ All files remain internally consistent
- ✅ Documentation updated to reflect changes
- ✅ Version numbers included
- ✅ CHANGELOG.md updated
- ✅ Deliverables are actual files (code, configs, CAD files, etc.)
- ✅ Output is manufacturing-ready (or marked as Concept Design)

---

## 📞 Questions?

If instructions are unclear or conflicting:

1. Ask the user for clarification
2. Reference the specific instruction file and line
3. Explain why the instruction is ambiguous
4. Suggest how to resolve it

---

**Last Updated:** 2026-08-04  
**Maintained by:** GitHub Copilot Integration  
**Authority:** MASTER_SPECIFICATION.md
