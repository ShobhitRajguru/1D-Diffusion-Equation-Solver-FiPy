# 1D Heat Diffusion Equation Solver Using FiPy

Finite Volume Method (FVM) implementation of the 1D transient heat diffusion equation using FiPy.

Features:
- Dirichlet, Neumann and Robin boundary conditions
- Source and no-source formulations
- Transient and steady-state analysis
- Mesh convergence study
- Time-step convergence study
- Numerical vs analytical validation
- Error analysis


## Overview

This repository presents the numerical solution of the one-dimensional heat diffusion equation using the Finite Volume Method (FVM) implemented in FiPy. The project investigates transient and steady-state heat diffusion under different boundary conditions and compares numerical results with analytical solutions.

The work was carried out as part of an M.Tech study in computational modeling and numerical methods.

## Objectives

* Solve the 1D heat diffusion equation using FiPy.
* Study Dirichlet, Neumann, and Robin boundary conditions.
* Investigate transient and steady-state behavior.
* Validate numerical solutions against analytical solutions.
* Perform mesh convergence and timestep convergence studies.
* Quantify numerical error and solution accuracy.

## Cases Studied

### Case 1: Dirichlet Boundary Condition (No Source)

* Fixed values at both boundaries.
* Analytical validation performed.

### Case 2: Dirichlet Boundary Condition (With Source)

* Uniform source term included.
* Analytical validation performed.

### Case 3: Modified Neumann Boundary Condition

* Zero-flux condition with additional constraint.
* Analytical validation performed.

### Case 4: Neumann Boundary Condition (With Source)

* Source-driven diffusion problem.
* Analytical validation performed.
  
### Case 5: Robin Boundary Condition (With Source)

* Mixed boundary condition with source term.
* Analytical and numerical comparison performed.
  
### Case 6: Robin Boundary Condition (No Source)

* Mixed boundary condition formulation.
* Steady-state behavior investigated.


## Numerical Method

The governing diffusion equation is solved using the Finite Volume Method (FVM) available in the FiPy PDE solver framework. Simulations include transient evolution toward steady state together with mesh independence and timestep independence studies.

## Software Environment

* Python 3.9.25
* FiPy 3.4.4
* NumPy 1.23.5
* SciPy 1.10.1
* Matplotlib 3.9.4
* JupyterLab 4.4.6

## Repository Structure

```text
Case_1_Dirichlet_NoSource/
Case_2_Dirichlet_Source/
Case_3_Modified_Neumann/
Case_4_Neumann_Source/
Case_5_Robin_Source/
Case_6_Robin_NoSource/
docs/
README.md
```

## Key Results

* Numerical solutions show excellent agreement with analytical solutions.
* Mesh convergence and timestep convergence were verified for all applicable cases.
* The study demonstrates the application of FiPy for solving diffusion problems with different boundary conditions.

## Future Work

* Extension to 2D heat conduction.
* Nonlinear material properties.
* Variable diffusion coefficients.
* Coupled multiphysics simulations.

