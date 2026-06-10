# Case 6: Robin Boundary Condition Without Internal Heat Generation

## Problem Description

This case investigates the numerical solution of the one-dimensional transient diffusion equation without internal heat generation using the Finite Volume Method (FVM) implemented in FiPy.

The computational domain extends from x = 0 to x = 1 with a Neumann boundary condition at the left boundary and a Robin (convective) boundary condition at the right boundary.

### Boundary Conditions

```text
dT/dx (0,t) = 0

dT/dx (1,t) + h[T(1,t) - T∞] = 0
```

### Physical Parameters

```text
k   = 1.0   (Diffusion Coefficient)
h   = 1.0   (Convective Heat Transfer Coefficient)
T∞  = 0.0   (Ambient Temperature)
L   = 1.0   (Domain Length)
```

No internal heat generation is present within the computational domain.

---

## Governing Equation

```math
\frac{\partial T}{\partial t}
=
k\frac{\partial^2 T}{\partial x^2}
```

where:

- T = temperature
- k = diffusion coefficient
- x = spatial coordinate
- t = time

---

## Analytical Solution

At steady state:

```math
\frac{d^2T}{dx^2}=0
```

Applying the boundary conditions:

```text
dT/dx (0) = 0

dT/dx (1) + h[T(1) - T∞] = 0
```

gives:

```math
T(x)=T_{\infty}
```

For the present study:

```text
T∞ = 0
```

Therefore:

```math
T(x)=0
```

This analytical solution is used to validate the numerical results.

---

## Numerical Setup

| Parameter | Value |
|------------|--------|
| Domain Length (L) | 1.0 |
| Diffusion Coefficient (k) | 1.0 |
| Convective Coefficient (h) | 1.0 |
| Ambient Temperature (T∞) | 0.0 |
| Number of Cells (nx) | 50 |
| Time Step (Δt) | 1 × 10⁻³ |
| Number of Time Steps | 2000 |

The temperature field was initialized according to the notebook implementation.

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

- The transient solution gradually relaxes toward thermal equilibrium.
- The insulated boundary prevents heat flux through the left boundary.
- The Robin boundary condition drives the solution toward the ambient temperature.
- The steady-state solution becomes uniform throughout the domain.
- Time-step convergence confirms temporal independence of the numerical solution.
- Mesh convergence confirms spatial independence of the numerical solution.
- Numerical and analytical solutions show near-perfect agreement.

### Error Metrics

```text
Maximum Error = 0
L2 Error      = 0
```

The numerical and analytical solutions overlap exactly, demonstrating the accuracy of the FiPy implementation for diffusion problems under Robin boundary conditions without internal heat generation.

---

## Files

- `Case_6.ipynb` – FiPy simulation notebook
- `Case_6_Report.pdf` – Detailed technical report
- `Results/` – Generated plots and figures

---

## Conclusion

The Finite Volume Method implemented in FiPy successfully reproduces the analytical solution of the one-dimensional diffusion equation without internal heat generation under Neumann–Robin boundary conditions. The numerical solution converges to the expected uniform steady-state temperature equal to the ambient temperature, while convergence studies and error analysis confirm the accuracy, stability, and robustness of the implementation.
