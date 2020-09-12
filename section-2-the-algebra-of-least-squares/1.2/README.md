# Lecture Note 1.2

by Qiang Gao, updated at March 26, 2018

## Chapter 1 Finite-Sample Properties of OLS

### Section 2 The Algebra of Least Squares

...

#### Residuals are NOT the error terms

* $$\boldsymbol{\beta}$$ is unknown
* overfitting

#### Basic Algebraic Problems

**Existence \(does there exist a solution?\)**

* For $$y = a x^2 + b x + c$$, there exists a solution only if $$b^2 \geq 4 a c$$.
* For $$\mathbf{y} = \mathbf{A} \mathbf{x}$$, there exists a solution only if $$\mathbf{y}$$ lies in the **column space** of $$\mathbf{A}$$.

**Uniqueness \(is the solution unique?\)**

* For $$y = a x^2 + b x + c$$, there exists a solution and the solution is unique only if $$b^2 = 4 a c$$.
* For $$\mathbf{y} = \mathbf{A} \mathbf{x}$$, there exists a solution and the solution is unique only if $$\mathbf{y}$$ lies in the **column space** of $$\mathbf{A}$$ and $$\mathbf{A}$$ has **full column rank**.

**Analytical Solution \(is the solution in closed-form?\)**

* If $$y = a x^2 + b x + c$$ and $$b^2 \geq 4 a c$$, then the solutions are $$x = (-b \pm \sqrt{b^2 - 4ac}) /(2a)$$.
* If $$\mathbf{y} = \mathbf{A} \mathbf{x}$$ and $$\mathbf{A}$$ is \(square and\) invertible, then the unique solution is $$\mathbf{x} = \mathbf{A}^{-1} \mathbf{y}$$.

#### Vector Differentiation

* For the real-valued function $$y = f( \mathbf{x} ) = \mathbf{a}' \mathbf{x}$$ \(inner product form\),

  $$
  \frac{df(\mathbf{x})}{d\mathbf{x}} = \mathbf{a}.
  $$

* For the real-valued function $$y = f( \mathbf{x} ) = \mathbf{x}' \mathbf{A} \mathbf{x}$$ \(quadratic from\),

  $$
  \frac{df(\mathbf{x})}{d\mathbf{x}} = \mathbf{A} \mathbf{x}.
  $$

#### Matrix Multiplication

There are equivalently _four_ ways of [matrix multiplication](../../supplements/matrix-multiplication.md), each is very important.

Copyright ©2018 by Qiang Gao

