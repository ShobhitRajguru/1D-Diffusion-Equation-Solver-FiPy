# Case 3: Mixed Boundary Conditions (Dirichlet–Neumann) Without Source Term

## Problem Description

This case investigates the numerical solution of the one-dimensional transient diffusion equation without a source term using the Finite Volume Method (FVM) implemented in FiPy.

The computational domain extends from (x=0) to (x=1) with mixed boundary conditions:

* Dirichlet boundary condition at the left boundary
* Neumann boundary condition at the right boundary

Boundary conditions:

* (y(0,t)=1)
* (\frac{dy}{dx}(1,t)=0)

The combination of a fixed-value boundary and a zero-flux boundary results in a constant steady-state solution throughout the domain.

---

## Governing Equation

```math
\frac{\partial y}{\partial t}
=
k\frac{\partial^2 y}{\partial x^2}
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

Applying the boundary conditions:

```math
y(0)=1
```

```math
\frac{dy}{dx}(1)=0
```

gives:

```math
y(x)=1
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

* The transient solution converges toward a uniform steady-state profile.
* Mixed Dirichlet–Neumann boundary conditions produce a constant steady-state solution.
* Time-step convergence confirms temporal independence of the numerical solution.
* Mesh convergence confirms spatial independence of the numerical solution.
* Numerical and analytical solutions show near-perfect agreement.
* Maximum Error:

```text
7.99 × 10⁻¹²
```

* L2 Error:

```text
5.64 × 10⁻¹²
```

The error is close to machine precision, demonstrating the accuracy of the FiPy implementation.

---

## Files

* `Case_3.ipynb` – FiPy simulation notebook
* `Case_3_Report.pdf` – Detailed technical report
* `Results/` – Generated plots and figures

---

## Conclusion

The Finite Volume Method implemented in FiPy successfully reproduces the analytical solution of the one-dimensional diffusion equation with mixed Dirichlet–Neumann boundary conditions. The numerical solution converges to the expected constant steady-state profile, while convergence studies and error analysis confirm the accuracy, stability, and robustness of the implementation.
