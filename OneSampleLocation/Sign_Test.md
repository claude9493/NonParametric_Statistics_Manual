# Sign Test

## Hypothesis

$H_0: \theta=\theta_0$

- One-sided Upper-Tail Test: $H_1: \theta > 0$, reject $H_0$ if $B\geq b_\alpha$
- One-sided Lower-Tail Test: $H_2: \theta < 0$, reject $H_0$ if $B\leq n-b_\alpha$
- Two-sided Test: $H_3: \theta\neq0$, reject $H_0$ if $B\geq b_{\alpha/2}$ or  $B\leq n-b_{\alpha/2}$

## Test Statistics
$$B = \sum_{i=1}^n\phi_i$$
$B$ is the number of postive $Z$'s. $\phi_i=I(Z_i>0)$

### Exact Distribution
$$B\sim Binomial(n, 1/2)$$
$$E_0(B)=\frac{n}{2},\quad Var_0(B)=\frac{n}{4}$$

## Large Sample Approximation

$$B^*=\frac{B-\frac{n}{2}}{\sqrt{\frac{n}{4}}}$$

## Ties

Discard the zero values and redefine $n$ to the number of **nonzero** $Z$'s.

## Exact Power of Sign Test

![](..\Figures\exact-power-sign-test.png)

## Estimator

$$\hat{\theta}=\left\{\begin{array}{cc}{Z^{(k+1)}} & {n=2 k+1} \\ {\frac{Z^{(k)}+Z^{(k+1)}}{2}} & {n=2 k}\end{array}\right.$$

!> In calculating the estimator of $\theta$, we use all the $Z$, not discard this time.

## Confidence Interval
### Symmetric 2-sided
$$(Z^{(C_\alpha),Z^{(n+1-C_\alpha)}})$$
$$C_\alpha=n+1-b_{\alpha/2}\sim\frac{n}{2}-z_{\alpha/2}\sqrt{\frac{n}{4}}$$
$b_{\alpha/2}$ is the upper $\alpha/2$ percentile point of the null distribution of $B$.

$inf_{\theta\in\Theta}P(L<\theta<U)\geq1-\alpha$
$P(C_\alpha \leq B\leq n-C_\alpha)\geq1-\alpha$
