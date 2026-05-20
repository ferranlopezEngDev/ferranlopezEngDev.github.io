# Nonlinear Solvers for Hydraulic Networks

## Overview

Hydraulic network simulation often leads to nonlinear equation systems where unknown heads or flows must satisfy conservation and loss relations simultaneously. Even small benchmark cases can be sensitive to initialization, scaling, model formulation, and stopping criteria.

This note is a compact reference for the solver ideas that are most relevant to the HN3Ttk project line.

## Residual formulation

A common way to represent a steady hydraulic network is to define a residual vector whose entries should be zero at the solution.

Typical ingredients include:

- Mass conservation at nodes
- Head-loss or energy-balance relations across connections
- Boundary-condition equations for known heads, injections, or other prescribed values

From a software perspective, this is useful because the physical model can be mapped into a generic nonlinear system:

```text
R(x) = 0
```

where `x` may contain unknown nodal heads, connection flows, or a mixed state representation depending on the chosen formulation.

## Solver families

### Newton-type methods

Newton-Raphson style methods are a natural first choice when a Jacobian can be assembled or approximated. They can converge quickly near a good solution, but they are also sensitive to initial guesses, model scaling, and singular or poorly conditioned Jacobians.

Typical concerns:

- Divergence from poor initial states
- Oscillation between iterations
- Oversized update steps
- Ill-conditioned Jacobians

### Damped Newton variants

Damping reduces step size when a full Newton update is too aggressive. This often improves robustness, especially in early iterations or in cases with strong nonlinear losses.

### Continuation or gradual loading

Continuation strategies solve a sequence of easier intermediate problems before reaching the final target case. In hydraulic networks this can help when direct convergence is difficult under the full load or full nonlinearity.

### SciPy root-based solvers

`scipy.optimize.root` is useful for comparison against custom implementations. It provides a practical way to test whether convergence problems come from the model formulation, the Jacobian logic, or the chosen custom step strategy.

### Least-squares formulations

Some nonlinear systems can also be studied through least-squares-style solution strategies. This does not replace physical interpretation, but it can be useful as a numerical comparison path when debugging residual behaviour.

## Practical checks

When assessing solver behaviour, the following checks are usually more informative than simply looking at a success flag:

- Residual norm trend per iteration
- Sensitivity to initial guesses
- Step size behaviour
- Whether the final state is physically plausible
- Consistency of units and scaling
- Comparison against small benchmark problems

For engineering work, solver convergence should not be separated from model validation. A converged answer is only useful if the formulation and assumptions are also correct.

## Relevance to HN3Ttk

HN3Ttk is a suitable environment for studying these topics because the project already combines:

- Residual-based hydraulic modelling
- Custom Newton-style solvers
- SciPy solver wrappers
- Small benchmark-style examples
- A toolkit-oriented architecture rather than a single fixed closed workflow

This makes it possible to compare solver behaviour on simple cases such as:

- Single pipe
- Parallel pipes
- Three-reservoir problem
- Simple looped network

## Current scope

This note is intentionally introductory. It does not attempt to be a full numerical analysis chapter or a formal solver manual.

Its main purpose is to anchor future project documentation around a few practical ideas:

- solver choice matters;
- convergence behaviour must be inspected, not assumed;
- residual formulation and model structure are tightly connected;
- validation cases are essential for credible engineering software.
