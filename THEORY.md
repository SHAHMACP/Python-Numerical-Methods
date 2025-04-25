# Theory for Numerical Methods

## Part A - Root Finding, Interpolation, Differentiation, and Integration

### 1. Bisection Method
The Bisection Method is a bracketing method for finding the root of a function f(x) where the function changes sign over an interval [a, b]. The interval is repeatedly halved until the root is approximated within a given tolerance. It is simple and reliable but converges slowly.

### 2. Newton-Raphson Method
An open method for solving f(x) = 0, it uses tangents to approximate the root. Starting from an initial guess x₀, it iterates using:
xₙ₊₁ = xₙ - f(xₙ)/f'(xₙ)
It has quadratic convergence near the root but may diverge if the initial guess is poor.

### 3. Lagrange Interpolation
This method estimates a function given a set of known data points using a polynomial. The interpolating polynomial is constructed as a weighted sum of basis polynomials, each of which is zero at all data points except one.

### 4. Newton’s Interpolation
Similar to Lagrange, but uses divided differences and builds the interpolating polynomial incrementally. It is more efficient for updating the polynomial when new data points are added.

### 5. Numerical Differentiation (Continuous Function)
Estimates the derivative f'(x) using finite differences. The central difference formula:
f'(x) ≈ (f(x + h) - f(x - h)) / (2h)
is accurate and widely used when f(x) is known analytically.

### 6. Numerical Differentiation (Tabulated Function)
Used when f(x) is known only at discrete points. The derivative at a point is approximated using neighboring values:
f'(xⱼ) ≈ (yⱼ₊₁ - yⱼ₋₁) / (2h)

### 7. Trapezoidal Rule of Integration
Approximates the definite integral ∫ₐᵇ f(x)dx by dividing the interval into n parts and summing up areas of trapezoids.

### 8. Simpson’s Rule of Integration
Uses parabolic segments to approximate the integral. Given an even number of intervals:
∫ₐᵇ f(x)dx ≈ h/3 [f(x₀) + 4f(x₁) + 2f(x₂) + ... + f(xₙ)]

## Part B - Solving Linear Systems and ODEs

### 9. Gauss Elimination with Pivoting
Transforms the system to upper triangular form by row operations and uses back substitution. Pivoting ensures numerical stability.

### 10. Gauss-Seidel Iteration
An iterative technique to solve linear systems. It improves each variable sequentially using the latest available values.

### 11. Euler’s Method
Solves ODEs of the form y' = f(x, y). Starting from an initial point:
yₙ₊₁ = yₙ + h*f(xₙ, yₙ)

### 12. Runge-Kutta Method (Order 2)
A second-order method that improves on Euler’s Method by computing an average slope:
yₙ₊₁ = yₙ + 1/2(k₁ + k₂)

### 13. Runge-Kutta Method (Order 4)
Computes four slopes per step and uses a weighted average:
yₙ₊₁ = yₙ + 1/6(k₁ + 2k₂ + 2k₃ + k₄)

### 14. Eigenvalue Evaluation
Computes the eigenvalues and eigenvectors of a matrix, important in linear algebra and stability analysis.