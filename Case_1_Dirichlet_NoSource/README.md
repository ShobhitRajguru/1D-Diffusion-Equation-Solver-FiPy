# Case 1: Dirichlet Boundary Condition Without Source

## Overview

This case solves the one-dimensional transient diffusion equation using the Finite Volume Method (FVM) implemented in FiPy.

## Governing Equation

∂y/∂t = k ∂²y/∂x²

## Boundary Conditions

* y(0) = 0
* y(1) = 1

## Analytical Solution

y(x) = x

## Studies Performed

* Transient evolution
* Steady-state verification
* Numerical vs analytical comparison
* Mesh convergence study
* Time-step convergence study
* Error analysis

## Files

* Case_1.ipynb — FiPy implementation
* Case_1_Report.docx — Detailed documentation and analysis
* figures/ — Simulation plots
