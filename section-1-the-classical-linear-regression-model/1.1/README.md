# Lecture Note 1.1

by Qiang Gao, updated at March 26, 2018

## Chapter 1 Finite-Sample Properties of OLS

### Section 1 The Classical Linear Regression Model

...

#### The Big Picture of Econometrics

Its a bridge between **model** and **data**. Model is some theoretic mathematical formulation. Data is collected/measured from the real world according to the definition of variables.

The bridge is in two ways:

1. \(from data to model\) Parameter Estimation.
2. \(from model to data\) Hypothesis Test.

#### Assumption 1.1 \(linearity\)

**1. It's a tautology**

Because the error term $$\varepsilon_i$$ is defined as

$$
\varepsilon_i = y_i - \mathbf{x}_i \cdot \boldsymbol\beta,
$$

the equality in \(1.1.1\) trivially holds true by definition.

Equation \(1.1.1\) only restricts a linear functional relationship between $$y$$ and $$\mathbf{x}$$, nothing more.

**2. Nonlinearity can be linearized**

The linearity assumption is not so much restrictive, because any nonlinear function can be easily [linearized](../../supplements/taylor-linearization.md).

**3. The knowns are \) and the unknowns are** 

**4.  is of primary interest**

$$\beta$$ means marginal separate effects.

**5.  is of primary concern**

$$\varepsilon_i$$ should not depend on $$\mathbf{x}$$

**6. marginal separate effect relies on total differentiation**

* explicit equation
* implicit equation
* differential vs. elasticity

**7. variables are usually transformed \(in log\)**

By the rules of differentiation

$$
\frac{d \ln x}{dx} = \frac{1}{x},
$$

we can write it in total differential form as

$$
d \ln x = \frac{dx}{x}.
$$

Similarly,

$$
d \ln y = \frac{dy}{y}.
$$

So

$$
\frac{d \ln y}{d \ln x} = \frac{d y / y}{d x / x}
$$

coincides with the definition of elasticity. It is of this reason that in economics, variables are often expressed in logs rather than in levels in equations.

#### Assumption 1.2 \(strict exogeneity\)

**Joint Distribution**

$$
f_{Y,X}(y, x) \qquad \oint f_{Y,X}(y, x)\,dx\,dy = 1
$$

**Marginal Distribution**

$$
\begin{align}
f_{Y} (y) \equiv \oint f_{Y,X}(y, x) \, dx && \oint f_{Y} (y) \, dy = 1 \\
f_{X} (x) \equiv \oint f_{Y,X}(y, x) \, dy && \oint f_{X} (x) \, dx = 1 
\end{align}
$$

**Conditional Distribution**

**\(Unconditional\) Expectation**

The \(unconditional\) expectation $$\mathrm{E}(x)$$ is defined as

$$
\mathrm{E}(x) = \int x f(y, x) \, dy dx
$$

**Conditional Expectation**

If $$(y, x)$$ are jointly distributed random variables, where their joint p.d.f. is expressed as $$f(y, x)$$, then $$\mathrm{E} (y | x)$$ is defined as

$$
\mathrm{E} (y|x) = \int_{-\infty}^{+\infty} y \frac{ f(y, x) }{ \int_{-\infty}^{+\infty} f(y, x) dy } dy,
$$

where $$\int_{-\infty}^{+\infty} f(y, x) dy$$ is the definition of the marginal distribution of $$x$$. In words, the expectation of $$y$$ conditional on $$x$$ is the weighted average of $$y$$, where the weighting is the conditional probability density.

**Law of Total Expectations**

$$
\mathrm{E} ( \mathrm{E} (y | x) ) = \mathrm{E} (y).
$$

**Law of Iterated Expectations**

$$
\mathrm{E} ( \mathrm{E} (y | x, z) | z ) = \mathrm{E} (y | z).
$$

**Moment**

The $$k$$-th order moment of a random variable $$x$$ is defined as

$$
\mathrm{E}(x^k)
$$

**Variance**

$$
\begin{align}
\mathrm{Var}(x) &= \mathrm{E} [ (x - \mathrm{E} (x))^2 ] && \text{(definition)} \\
&= \mathrm{E}(x^2)- E(x)^2 && \text{(formula)}
\end{align}
$$

**Covariance**

$$
\begin{align}
\mathrm{Cov} (x, y) &= \mathrm{E} [ (x - \mathrm{E} (x) )( y - \mathrm{E} (y)) ] && \text{(definition)} \\
&= \mathrm{E} (xy) - \mathrm{E}(x) \mathrm{E} (y) && \text{(formula)}
\end{align}
$$

**Correlation Coefficient**

$$
\rho_{x,y} = \frac{\mathrm{Cov} (x,y)}{\sqrt {\mathrm{Var} (x) \mathrm{Var} (y)}} \in [-1, 1]
$$

**Linearity of Expectation**

$$
\mathrm{E} (ax + b) = a \mathrm{E} (x) + b
$$

**Nonlinearity of Variance**

$$
\mathrm{Var} (ax + b) = a^2 \mathrm{Var} (x).
$$

#### Assumption 1.3 \(no multicollinearity\)

* perfect multicollinearity _can_ occur in rare conditions as long as its _measure_ is zero.

#### Assumption 1.4 \(spherical error variance\)

$$
\mathbf{x} \mathbf{x}'
\equiv
\begin{bmatrix}
x_1^2 & \cdots & x_1 x_n \\
\vdots & \ddots & \vdots \\
x_n x_1 & \cdots & x_n^2
\end{bmatrix}
$$

$$
\mathrm{E}
\begin{bmatrix}
a_{11} & \cdots & a_{n1} \\
\vdots & \ddots & \vdots \\
a_{m1} & \cdots & a_{mn}
\end{bmatrix}
\equiv
\begin{bmatrix}
\mathrm{E} (a_{11}) & \cdots & \mathrm{E} (a_{n1}) \\
\vdots & \ddots & \vdots \\
\mathrm{E} (a_{m1}) & \cdots & \mathrm{E} (a_{mn})
\end{bmatrix},
$$

$$
\mathrm{Var} ( \mathbf{x} )
\equiv
\mathrm{E} [ ( \mathbf{x} - \overline{\mathbf{x}} ) ( \mathbf{x} - \overline{\mathbf{x}} )' ]
$$

Copyright ©2018 by Qiang Gao

