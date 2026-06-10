# Case 2: Dirichlet Boundary Condition (With Source Term)

## Problem Description

This case investigates the numerical solution of the one-dimensional transient diffusion equation with a constant source term using the Finite Volume Method (FVM) implemented in FiPy.

The computational domain extends from (x=0) to (x=1) with fixed Dirichlet boundary conditions imposed at both ends:

* (y(0,t)=0)
* (y(1,t)=1)

A uniform source term is present throughout the domain, causing the steady-state solution to become parabolic rather than linear.

---

## Governing Equation

```math
\frac{\partial y}{\partial t}
=
k\frac{\partial^2 y}{\partial x^2}
+ S
```

where:

* (y) = dependent variable
* (k) = diffusion coefficient
* (S) = source term
* (x) = spatial coordinate
* (t) = time

For this study:

* Diffusion coefficient (k = 1)
* Source term (S = 1)
* Domain length (L = 1)

---

## Analytical Solution

At steady state:

```math
\frac{d^2y}{dx^2}+1=0
```

Applying the Dirichlet boundary conditions gives:

```math
y(x)= -\frac{x^2}{2}+\frac{3}{2}x
```

This analytical solution is used to validate the numerical results.

---

## Numerical Setup

| Parameter                 | Value    |
| ------------------------- | -------- |
| Domain Length (L)         | 1.0      |
| Diffusion Coefficient (k) | 1.0      |
| Source Term (S)           | 1.0      |
| Number of Cells (nx)      | 50       |
| Time Step (Δt)            | 1 × 10⁻³ |
| Number of Time Steps      | 2000     |

Initial Condition:

```math
y(x,0)=\sin(\pi x)
```

---

## Studies Performed

* Transient evolution analysis
* Time-step convergence study
* Mesh convergence study
* Steady-state verification
* Numerical vs analytical comparison
* Error analysis

---

## Key Results

* The transient solution converges smoothly toward the steady-state profile.
* The source term produces a parabolic steady-state solution.
* Time-step convergence confirms temporal independence of the numerical solution.
* Mesh convergence confirms spatial independence of the numerical solution.
* Numerical and analytical solutions show excellent agreement.
* Maximum Error:

```text
5.0 × 10⁻⁵
```

* L2 Error:

```text
5.0 × 10⁻⁵
```

The low error magnitude demonstrates the accuracy of the FiPy implementation for diffusion problems with internal generation.

---

## Files

* `Case_2.ipynb` – FiPy simulation notebook
* `Case_2_Report.pdf` – Detailed technical report
* `Results/` – Generated plots and figures

---

## Conclusion

The Finite Volume Method implemented in FiPy successfully reproduces the analytical solution of the one-dimensional diffusion equation with a constant source term and Dirichlet boundary conditions. Convergence studies, steady-state verification, and error analysis confirm the accuracy, stability, and reliability of the numerical implementation.
