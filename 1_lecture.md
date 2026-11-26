## Kinds of market models:
* Discrete time models
  * Single period
  * Multi period
* Continuous time models

## Financial Economics vs Financial Engineering

Financial Economics: Use equilibrium arguments to
* Price equities, bonds and other assets
* Set interest rates

Financial Engineering: Assume prices of equities and interest rates given

* Price derivatives on equities, bonds, interest rates, etc., using the
no-arbitrage condition

Not even close to being a complete separation
* For example, Capital Asset Pricing Model of interest to both

**Financial economics** examines why markets behave as they do—studying equilibrium, interest rates, risk premia, and policy impacts 
—while **financial engineering** applies advanced math, statistics, and programming to build, price, and hedge financial instruments and trading systems.

## Conditional Probability

Conditional probability is the probability of an event $A$ occurring given that another event $B$ is already known to have occurred. 
It is written as $P(A \mid B)$ and read as "the probability of A given B".

## Law of the unconscious statistician (LOTUS) theorem

Expresses the expected value of a function $g(X)$ of a random variable $X$ in terms of $g$ and the probability distribution of $X$.

For discrete distribution of $X$ with known prob mass function $p_X$,
$$E[g(X)] = \sum_{x \in X}{g(x) p_X(x)}$$
For continious distribution of $X$ with prob density funcion $f_X$,
$$E[g(X)] = \int_{-\infty}^{\infty} g(x)f_X(x)dx$$

## Moment generating function (MGF)

Used in probability and statistics to calculate the moments of a random variable—such as its mean and variance—and to uniquely identify or analyze probability distributions.

Defined as $M_X(t) = \mathbb{E}[e^{tX}]$ (when it exists near $t=0$), it turns complex probability calculations into simpler algebraic or calculus steps.

### Key Uses
* Finding moments easily: Taking the $n$-th derivative of the MGF and evaluating it at $t = 0$ gives the $n$-th raw moment, $\mathbb{E}[X^n]$. The first derivative at $0$ gives the mean $\mathbb{E}[X]$, and combining the first and second derivatives gives the variance $\mathbb{E}[X^2] - (\mathbb{E}[X])^2$.
* Identifying distributions (uniqueness): If an MGF exists on an open interval around $0$, it uniquely determines the probability distribution. 
Matching a formula to a known MGF lets you identify the distribution without inverting integrals or sums.
* Sums of independent random variables: The MGF of a sum of independent random variables equals the product of their individual MGFs, which simplifies finding the distribution of sums.
* Proving theorems and tail bounds: MGFs are used to prove limit theorems like the Central Limit Theorem and to derive tail probability bounds such as Chernoff bounds

## Independent random variables product expectation and variance.

If random variables $X$ and $Y$ are independent, the expectation of their product equals the product of their individual expectations: 
$\mathbb{E}[XY] = \mathbb{E}[X]\mathbb{E}[Y]$

For two independent random variables $X$ and $Y$, the variance of their product is:
$$Var(XY) = Var(X)Var(Y) + Var(X) [\mathbb{E}(Y)]^2 + Var(Y) [\mathbb{E}(X)]^2$$
Equivalently, using expectations:
$$Var(XY) = \mathbb{E}(X^2)\mathbb{E}(Y^2) - [\mathbb{E}(X)]^2[\mathbb{E}(Y)]^2$$