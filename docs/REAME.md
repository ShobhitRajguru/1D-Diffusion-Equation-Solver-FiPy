# 1D Heat Diffusion Using FiPy

## Finite Volume Analysis of the 1D Heat Diffusion Equation Under Dirichlet, Neumann, and Robin Boundary Conditions


---

# Case 1: Dirichlet Boundary Condition Without Source

## 1. Problem Statement

The objective of this case study is to solve the one-dimensional transient diffusion equation using FiPy under Dirichlet boundary conditions without any internal source term. The computational domain extends from x = 0 to x = 1. Constant values are prescribed at both boundaries, with y = 0 at the left boundary and y = 1 at the right boundary.

Since the original problem statement specifies only the governing equation and boundary conditions, an initial condition is required to perform transient numerical simulations. Therefore, the initial profile is assumed as y(x,0) = sin(πx).

The transient solution is evolved in time using the finite volume method implemented in FiPy. As time progresses, the solution converges to the corresponding steady-state solution. Additional studies including numerical–analytical comparison, mesh convergence, timestep convergence, and error analysis are performed to verify the accuracy and stability of the numerical implementation.
