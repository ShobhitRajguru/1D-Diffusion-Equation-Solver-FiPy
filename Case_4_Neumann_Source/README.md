# Case 4: Mixed Boundary Conditions (Dirichlet–Neumann) With Source Term

## Problem Description

This case investigates the numerical solution of the one-dimensional transient diffusion equation with a constant source term using the Finite Volume Method (FVM) implemented in FiPy.

The computational domain extends from x = 0 to x = 1 with mixed boundary conditions consisting of a Dirichlet condition at the left boundary and a Neumann condition at the right boundary.

### Boundary Conditions

```text
y(0,t) = 0
dy/dx (1,t) = 0
```

### Source Term

```text
S = 1
```

The presence of the source term together with the mixed boundary conditions results in a parabolic steady-state solution throughout the domain.

---

## Governing Equation

```math
\frac{\partial y}{\partial t}
=
k\frac{\partial^2 y}{\partial x^2}
+ S
```

where:

- y = dependent variable
- k = diffusion coefficient
- S = source term
- x = spatial coordinate
- t = time

For this study:

- Diffusion coefficient k = 1
- Source term S = 1
- Domain length L = 1

---

## Analytical Solution

At steady state:

```math
\frac{d^2y}{dx^2}+1=0
```

Applying the boundary conditions:

```text
y(0) = 0
dy/dx (1) = 0
```

gives:

```math
y(x)=x-\frac{x^2}{2}
```

This analytical solution is used to validate the numerical results.

---

## Numerical Setup

| Parameter | Value |
|------------|--------|
| Domain Length (L) | 1.0 |
| Diffusion Coefficient (k) | 1.0 |
| Source Term (S) | 1.0 |
| Number of Cells (nx) | 50 |
| Time Step (Δt) | 1 × 10⁻³ |
| Number of Time Steps | 2000 |

Initial Condition:

```text
y(x,0) = sin(πx)
```

---

## Studies Performed

- Transient evolution analysis
- Time-step convergence study
- Mesh convergence study
- Steady-state verification
- Numerical vs analytical comparison
- Error analysis

---

## Key Results

- The transient solution converges toward the expected parabolic steady-state profile.
- Internal generation introduces curvature into the solution.
- Mixed Dirichlet–Neumann boundary conditions are accurately enforced.
- Time-step convergence confirms temporal independence of the numerical solution.
- Mesh convergence confirms spatial independence of the numerical solution.
- Numerical and analytical solutions show excellent agreement.

### Error Metrics

```text
Maximum Error = 1.25 × 10⁻⁵
L2 Error      = 1.25 × 10⁻⁵
```

The low error magnitude demonstrates the accuracy of the FiPy implementation for diffusion problems with internal generation.

---

## Files

- `Case_4.ipynb` – FiPy simulation notebook
- `Case_4_Report.pdf` – Detailed technical report
- `Results/` – Generated plots and figures

---

## Conclusion

The Finite Volume Method implemented in FiPy successfully reproduces the analytical solution of the one-dimensional diffusion equation with a constant source term under mixed Dirichlet–Neumann boundary conditions. The numerical solution converges to the expected parabolic steady-state profile, while convergence studies and error analysis confirm the accuracy, stability, and robustness of the implementation.
