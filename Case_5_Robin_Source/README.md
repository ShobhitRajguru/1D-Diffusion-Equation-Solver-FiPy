# Case 5: Robin Boundary Condition With Internal Heat Generation

## Problem Description

This case investigates the numerical solution of the one-dimensional transient diffusion equation with uniform internal heat generation using the Finite Volume Method (FVM) implemented in FiPy.

The computational domain extends from x = 0 to x = 1 with a Neumann boundary condition at the left boundary and a Robin (convective) boundary condition at the right boundary.

### Boundary Conditions

```text
dT/dx (0,t) = 0

-k dT/dx (L,t) = h[T(L,t) - T∞]
```

### Physical Parameters

```text
k   = 1.0   (Diffusion Coefficient)
q̇   = 1.0   (Volumetric Heat Generation Rate)
h   = 1.0   (Convective Heat Transfer Coefficient)
T∞  = 0.0   (Ambient Temperature)
L   = 1.0   (Domain Length)
```

The presence of internal heat generation together with convective heat loss produces a parabolic steady-state temperature distribution.

---

## Governing Equation

```math
\frac{\partial T}{\partial t}
=
k\frac{\partial^2 T}{\partial x^2}
+
\dot q
```

where:

- T = temperature
- k = diffusion coefficient
- q̇ = volumetric heat generation rate
- x = spatial coordinate
- t = time

---

## Analytical Solution

At steady state:

```math
\frac{d^2T}{dx^2}
+
\frac{\dot q}{k}
=
0
```

Applying the Neumann and Robin boundary conditions gives:

```math
T(x)
=
T_{\infty}
+
\frac{\dot q L}{h}
+
\frac{\dot q}{2k}
\left(
L^2 - x^2
\right)
```

For:

```text
T∞ = 0
q̇  = 1
k  = 1
h  = 1
L  = 1
```

the solution becomes a parabolic temperature distribution throughout the domain.

This analytical solution is used to validate the numerical results.

---

## Numerical Setup

| Parameter | Value |
|------------|--------|
| Domain Length (L) | 1.0 |
| Diffusion Coefficient (k) | 1.0 |
| Heat Generation Rate (q̇) | 1.0 |
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

- The transient solution converges toward the expected parabolic temperature profile.
- Internal heat generation continuously increases the temperature within the domain.
- The insulated boundary prevents heat loss at the left boundary.
- The Robin boundary condition accurately models convective heat transfer at the right boundary.
- Time-step convergence confirms temporal independence of the numerical solution.
- Mesh convergence confirms spatial independence of the numerical solution.
- Numerical and analytical solutions show excellent agreement.

### Error Metrics

```text
Maximum Error = 1.25 × 10⁻⁵
L2 Error      = 1.25 × 10⁻⁵
```

The low error magnitude demonstrates the accuracy of the FiPy implementation for diffusion problems with internal heat generation and convective boundary conditions.

---

## Files

- `Case_5.ipynb` – FiPy simulation notebook
- `Case_5_Report.pdf` – Detailed technical report
- `Results/` – Generated plots and figures

---

## Conclusion

The Finite Volume Method implemented in FiPy successfully reproduces the analytical solution of the one-dimensional diffusion equation with internal heat generation under Neumann–Robin boundary conditions. The numerical solution converges to the expected parabolic steady-state temperature distribution, while convergence studies and error analysis confirm the accuracy, stability, and robustness of the implementation.
