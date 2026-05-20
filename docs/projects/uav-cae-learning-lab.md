# UAV CAE Learning Lab

## Overview

This project is a progressive technical learning line focused on fixed-wing electric UAV design foundations and open-source CAD/CAE workflows. The goal is not to present a final UAV immediately, but to build theory, documentation, CAD practice, and small simulation exercises step by step.

It combines aerodynamic foundations, lightweight structural thinking, geometry studies, meshing practice, introductory FEA and CFD cases, and Python-supported engineering workflows.

## Learning Philosophy

This section is intentionally framed as a learning laboratory. Configuration, airfoil selection, propulsion choices, and structural layout are not treated as finalized.

The aim is to move from theory to small validated exercises. Classical aerodynamics foundations, including John D. Anderson's *Fundamentals of Aerodynamics*, are part of the intended reference background for the study path.

## Technical Areas

- Fixed-wing UAV design
- UAV configurations
- Aerodynamics
- Flight mechanics foundations
- Aircraft geometry
- Stability basics
- Propulsion basics
- Lightweight structures
- CAD modelling
- Mesh generation
- Finite element learning cases
- CFD learning cases
- Open-source CAE workflows

## Toolchain

- FreeCAD
- SolveSpace
- OpenSCAD
- Gmsh
- Code_Aster
- OpenFOAM
- ParaView
- Python
- XFOIL
- XFLR5
- AVL
- SU2 as a possible later comparison tool for CFD learning cases

## Manufacturing Constraints

Early concepts should avoid assuming access to a 3D printer. Initial manufacturable studies are intended to stay compatible with accessible materials and processes such as:

- Sheet materials
- Commercial tubes
- Screws and fasteners
- Adhesives
- Foam board
- Plywood
- Balsa
- G10
- Carbon tubes
- Aluminium profiles

## Current Study Blocks

- Fixed-wing configuration comparisons and terminology
- Airfoil behaviour and polar interpretation
- Basic wing geometry parameterization
- Stability and flight mechanics foundations
- Structural idealization for simple lightweight members
- CAD exercises oriented toward sheet and tube-based assemblies
- Introductory meshing and solver setup workflows

## Planned CAD/CAE Exercises

| Exercise | Purpose |
| --- | --- |
| Basic wing geometry parameterization | Connect aerodynamic assumptions with simple geometry generation |
| Airfoil polar study | Compare profiles and interpret lift/drag trends with XFOIL or XFLR5 |
| Simple beam structural analysis | Build intuition for lightweight structural response |
| Gmsh meshing exercises | Learn mesh control on small representative geometries |
| Introductory OpenFOAM cases | Establish CFD workflow fundamentals on simple cases |
| CAD exercises for sheet and tube-based assemblies | Keep manufacturability assumptions realistic and accessible |
| Simple aerodynamic comparison studies | Compare configurations or parameter changes without overclaiming design maturity |

## Current Status

Early learning phase.

This is not yet a complete UAV design. It should be read as a structured learning programme with engineering intent, not as a finalized aircraft configuration.

## Next Steps

- Consolidate the first set of theory notes for aerodynamics and basic flight mechanics
- Build small CAD exercises with simple manufacturable constraints
- Add introductory meshing and post-processing examples
- Document at least one simple structural and one simple aerodynamic comparison case
- Clarify how this learning line connects to broader CAD/CAE and automation work in the portfolio
