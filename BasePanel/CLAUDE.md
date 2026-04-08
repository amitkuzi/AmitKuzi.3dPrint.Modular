# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

This is a FreeCAD parametric design project for a **modular panel system**. The primary design file is `Modular.FCStd`, with 3MF exports for 3D printing in 8x8 and 8x16 body variants.

## File Types

| Extension | Purpose |
|-----------|---------|
| `.FCStd` | FreeCAD source file — primary design artifact |
| `.FCBak` | FreeCAD automatic backup — do not commit |
| `.3mf` | 3D printing export — sliced/prepared for printing |
| `.oca` | Open CAD exchange format export |
| `.FCStd.*` | FreeCAD lock/temp files — do not commit |

## FreeCAD Operations

Run FreeCAD headless analysis or scripting via:

```bash
"C:/Program Files/FreeCAD 1.0/bin/freecadcmd.exe" <script.py>
```

The `niagara_analysis.py` script in `C:\Users\Amit.kuzi\OneDrive\LLMShared\Team_workspace\` shows the pattern for headless shape validation, bounding box, wall thickness, and fillet analysis — reuse it as a template for any new analysis scripts.

## Branching

This repo is managed under the broader LLMShared workspace conventions:

| Branch | Use |
|--------|-----|
| `main` | Stable, printable milestones |
| `Development` | Active design work |

Commit messages should be descriptive of the design state (e.g., `BodyMid8x8`, `V2`).

## Workspace Integration

The CAD Expert agent (defined in `C:\Users\Amit.kuzi\OneDrive\LLMShared\team\cad_expert.md`) owns this repository. Tasks, handoffs, and deliverables follow the LLMShared pipeline:

```
tasks/ → handoffs/ → drafts/ → [Validator] → inbox/
```

Design analysis outputs go to `C:\Users\Amit.kuzi\OneDrive\LLMShared\Team_workspace\` as handoff files.
