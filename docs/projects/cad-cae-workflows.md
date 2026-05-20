# CAD/CAE Open-Source Workflows

## Overview

This project line collects small studies and workflows using open-source CAD, meshing, simulation, and post-processing tools. The goal is to understand how to move from geometry to mesh, analysis, and interpretation in a reproducible way.

It supports both the UAV learning work and future structural or mechanical analysis projects. The intended emphasis is on workflow clarity rather than on large or visually complex models.

## Purpose

This section is meant to gather small practical examples that can be repeated, compared, and documented cleanly. It should help answer questions such as:

- How is geometry prepared before meshing?
- Which modelling simplifications are acceptable for a first study?
- How does mesh choice affect interpretation?
- What should be documented so that a case can be reproduced later?

## Toolchain

- FreeCAD
- SolveSpace
- OpenSCAD
- OpenCascade / OCCT
- picoGK
- Gmsh
- Code_Aster
- CalculiX
- Elmer FEM
- OpenFOAM
- SU2
- ParaView
- SALOME
- Python

## Workflow Philosophy

- Prefer small reproducible examples over large unfinished assemblies
- Keep geometry, assumptions, mesh settings, and result interpretation explicit
- Use the workflow itself as a learning object, not only the final result
- Reuse simple benchmark-like cases where possible
- Support future cross-links with reports and technical notes

## Planned Learning Cases

| Learning case | Purpose |
| --- | --- |
| Simple bracket model | Basic geometry preparation and structural idealization |
| Beam under bending | Compare simple analytical intuition with FEA setup |
| Plate with hole | Study stress concentration and meshing choices |
| Mesh convergence study | Build discipline around result quality and interpretation |
| Basic CFD channel or external flow case | Document a minimal fluid workflow |
| CAD-to-mesh workflow | Track handoff issues between modelling and meshing tools |
| Parametric geometry generation | Explore scripting and repeatable geometry variants |
| Post-processing screenshots and interpretation notes | Improve result communication and technical reporting |

## Current Status

Planned / learning phase.

The section is currently defined as a workflow collection rather than as a finished set of published case studies.

## Next Steps

- Publish a first small geometry-to-mesh example
- Add one structural and one CFD-oriented learning case
- Document solver assumptions and result interpretation more explicitly
- Define a consistent format for future case study notes and reports
