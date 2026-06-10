# Case 1: Dirichlet Boundary Condition (No Source)

## Problem Description

This case investigates the numerical solution of the one-dimensional transient diffusion equation without an internal source term using the Finite Volume Method (FVM) implemented in FiPy.

The computational domain extends from (x=0) to (x=1) with fixed Dirichlet boundary conditions imposed at both ends:

* (y(0,t)=0)
* (y(1,t)=1)

The transient solution is evolved in time until the steady-state solution is reached.

---

## Governing Equation

```math
\frac{\partial y}{\partial t}
=
k \frac{\partial^2 y}{\partial x^2}
```

where:

* (y) = dependent variable
* (k) = diffusion coefficient
* (x) = spatial coordinate
* (t) = time

For this study:

* Diffusion coefficient (k = 1)
* Domain length (L = 1)

---

## Analytical Solution

At steady state:

```math
\frac{d^2y}{dx^2}=0
```

Applying the boundary conditions gives:

```math
y(x)=x
```

This analytical solution is used to validate the numerical results.

---

## Numerical Setup

| Parameter                 | Value    |
| ------------------------- | -------- |
| Domain Length (L)         | 1.0      |
| Diffusion Coefficient (k) | 1.0      |
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
* Time-step convergence confirms temporal independence of the numerical solution.
* Mesh convergence confirms spatial independence of the numerical solution.
* Numerical and analytical solutions show excellent agreement.
* Maximum error:

```text
4.53 × 10⁻¹⁴
```

* L2 Error:

```text
3.25 × 10⁻¹⁴
```

The error is close to machine precision, demonstrating the accuracy of the FiPy implementation.

---

## Files

* `Case_1.ipynb` – FiPy simulation notebook
* `Case_1_Report.pdf` – Detailed technical report
* `Results/` – Generated plots and figures

---

## Conclusion

The Finite Volume Method implemented in FiPy successfully reproduces the analytical solution for the one-dimensional diffusion equation with Dirichlet boundary conditions. Convergence studies and error analysis confirm the accuracy, stability, and reliability of the numerical implementation.
