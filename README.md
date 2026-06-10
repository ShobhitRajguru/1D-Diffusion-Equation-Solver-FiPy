# 1D Heat Diffusion Equation Solver Using FiPy

Finite Volume Method (FVM) implementation of the one-dimensional transient heat diffusion equation using FiPy.

## Features

* Dirichlet, Neumann, and Robin boundary conditions
* Source and no-source formulations
* Transient and steady-state analysis
* Mesh convergence study
* Time-step convergence study
* Numerical vs analytical validation
* Error analysis

---

## Overview

This repository presents the numerical solution of the one-dimensional heat diffusion equation using the Finite Volume Method (FVM) implemented in FiPy. The project investigates transient and steady-state heat diffusion under different boundary conditions and compares numerical results with analytical solutions.

The work was carried out as part of an M.Tech study in computational modeling and numerical methods.

---

## Governing Equation

The one-dimensional transient heat diffusion equation considered in this work is

```math
∂T/∂t = α ∂²T/∂x² + S
```

where:

* **T** = temperature
* **α** = thermal diffusivity
* **S** = volumetric source term

---

## Objectives

* Solve the 1D heat diffusion equation using FiPy.
* Study Dirichlet, Neumann, and Robin boundary conditions.
* Investigate transient and steady-state behavior.
* Validate numerical solutions against analytical solutions.
* Perform mesh convergence and timestep convergence studies.
* Quantify numerical error and solution accuracy.

---

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

* Mixed boundary condition without source term.
* Analytical and numerical comparison performed.

---

## Numerical Method

The governing diffusion equation is solved using the Finite Volume Method (FVM) available in the FiPy PDE solver framework. Simulations include transient evolution toward steady state together with mesh independence and timestep independence studies.

---

## Software Environment

* Python 3.9.25
* FiPy 3.4.4
* NumPy 1.23.5
* SciPy 1.10.1
* Matplotlib 3.9.4
* JupyterLab 4.4.6

---

## Installation

Clone the repository:

```bash
git clone https://github.com/ShobhitRajguru/1D-Diffusion-Equation-Solver-FiPy.git
cd 1D-Diffusion-Equation-Solver-FiPy
```

Install the required packages:

```bash
pip install fipy numpy scipy matplotlib jupyterlab
```

---

## Repository Structure

```text
1D-Diffusion-Equation-Solver-FiPy
│
├── Case_1_Dirichlet_NoSource
├── Case_2_Dirichlet_Source
├── Case_3_Modified_Neumann
├── Case_4_Neumann_Source
├── Case_5_Robin_Source
├── Case_6_Robin_NoSource
└── README.md
```

---

## Key Results

* Numerical solutions showed excellent agreement with analytical solutions across all analytically solvable cases.
* Mesh convergence studies confirmed grid-independent solutions.
* Timestep convergence studies verified temporal accuracy and stability.
* Error analysis demonstrated very small numerical errors, often approaching machine precision.
* Dirichlet, Neumann, and Robin boundary conditions were successfully implemented and validated using the Finite Volume Method.
* The study demonstrates the effectiveness of FiPy for solving transient and steady-state diffusion problems.

---

## Future Work

* Extension to two-dimensional heat conduction.
* Nonlinear material properties.
* Variable diffusion coefficients.
* Coupled multiphysics simulations.
* Extension to semiconductor transport and diffusion problems.

---

## Author

**Shobhit Rajguru**

M.Tech – Semiconductor Materials and Devices (SMD)
Department of Materials Science and Metallurgical Engineering
Indian Institute of Technology Hyderabad
