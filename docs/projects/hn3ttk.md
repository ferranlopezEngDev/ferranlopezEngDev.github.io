# HN3Ttk — Hydraulic Network Toolkit

## Overview

HN3Ttk is an in-development hydraulic network modelling toolkit intended for building, solving, and experimenting with steady incompressible hydraulic network models. At this stage it should be understood as an engineering software learning and development project rather than as a finished industrial-grade simulator.

The current direction is closer to a flexible toolkit or framework than to a closed end-user application. The emphasis is on modelling abstractions, solver behaviour, validation cases, and documentation that can support later refinement.

## Origin: Hydranet as Legacy Prototype

HN3Ttk evolved from an earlier academic prototype called Hydranet, developed around final degree project work. Hydranet was useful as a first proof of concept for hydraulic network simulation, but it is now considered obsolete as a standalone direction.

The main lesson from that first implementation was that a cleaner and more extensible structure was needed. HN3Ttk is intended to keep the useful modelling ideas while moving toward a more modular, programmatic, and maintainable architecture.

For historical context, the earlier prototype is still documented in [Hydranet TFG — Legacy Prototype](hydranet-tfg.md).

## Technical Motivation

Hydraulic networks provide a good engineering setting for combining physical modelling with numerical methods and software design. Even relatively small cases require clear treatment of boundary conditions, nonlinear losses, solver robustness, and model representation.

This project is also a way to study how engineering models can be represented in software without hard-coding a single narrow workflow. That includes components, connections, residual formulation, validation cases, and solver strategies that can be refined progressively.

## Technical Areas

- Hydraulic networks
- Nonlinear equation systems
- Numerical solvers
- Engineering model abstraction
- Python software architecture
- Residual-based modelling
- Boundary conditions
- Hydraulic components
- Validation cases
- Technical documentation

## Main Technologies

- Python
- C++
- NumPy
- SciPy
- pandas
- matplotlib
- Markdown
- LaTeX
- GNU Octave
- OpenModelica

## Modelling Concepts

- Steady incompressible hydraulic networks
- Nodes and connections
- Mass conservation at nodes
- Energy balance across components
- Distributed head losses
- Darcy-Weisbach concepts
- Power-law loss approximations
- Pumps, valves, reservoirs, pipes, and special connections as future or conceptual components
- Solver strategies such as Newton-type methods, `scipy.optimize.root`, continuation or gradual loading, and robustness improvements

## Planned / Current Capabilities

| Capability | Current interpretation |
| --- | --- |
| Programmatic model definition | Central design goal |
| Residual formulation for network equations | Core modelling direction |
| Basic component abstraction | In development |
| Boundary condition handling | In development |
| Solver experiments and convergence checks | Active learning and testing area |
| SciPy-based solver wrappers and alternative nonlinear strategies | Present in the current public repository and still evolving |
| Validation against small benchmark problems | Active direction with public benchmark-style examples |
| Result export and tutorial-oriented examples | Present in the current public repository |
| Extended component library | Planned |
| Industrial-style packaging or GUI workflows | Not the current goal |

Some capabilities are still conceptual or experimental. The current priority is clarity of formulation and robustness on small cases, not feature breadth.

## Planned Case Studies

| Case study | Purpose |
| --- | --- |
| Three-reservoir problem | Check formulation of heads, losses, and nonlinear solver behaviour |
| Parallel pipes | Compare flow distribution and head-loss approximations |
| Simple looped network | Test coupled residual structure and convergence behaviour |
| Head-loss approximation comparisons | Study modelling sensitivity and implementation choices |
| Solver convergence experiments | Compare Newton-type strategies, `SciPy root`, and robustness improvements |
| API examples for model creation | Document intended usage as a toolkit rather than a closed application |

## Current Status

In development.

The project direction is active, but the documented scope should still be treated as early-stage. It is not presented as a finished simulator, and some components or solver strategies may remain planned until smaller validation cases are stable and clearly documented.

## Next Steps

- Consolidate the core model abstraction for nodes, connections, and boundary conditions
- Build and document a small set of benchmark hydraulic cases
- Compare alternative loss formulations and solver strategies
- Clarify which functionality belongs in the core toolkit and which should stay as examples or experiments
- Expand technical notes that explain solver behaviour and modelling assumptions

## Repository Links

- [Projects overview](index.md)
- [HN3Ttk repository](https://github.com/ferranlopezEngDev/HN3Ttk)
- [Technical note: Nonlinear Solvers for Hydraulic Networks](../technical-notes/nonlinear-solvers-hydraulic-networks.md)
- [Hydranet TFG — Legacy Prototype](hydranet-tfg.md)
- [hydranet_tfg legacy repository](https://github.com/ferranlopezEngDev/hydranet_tfg)
- [Portfolio repository](https://github.com/ferranlopezEngDev/ferranlopezEngDev.github.io)
