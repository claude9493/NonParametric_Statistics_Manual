# Ansari-Bradley Test

## Assumption
An additional assumption for Ansari-Bradley Test:

**A3.** The median $\theta_1$ of the $X$ population is equal to the median $\theta_2$ of the $Y$ population.

- $\frac{X-\theta}{\eta_{1}} \stackrel{d}{=} \frac{Y-\theta}{\eta_{2}}$
- If $\theta_1$ and $\theta_2$ are not equal but known, the shifted variables will satisfy the assumptions.

## Hypothesis
$$H_0: \gamma^2=\frac{\operatorname{Var}(X)}{\operatorname{Var}(Y)}=1$$
- $H_1: \gamma^2 > 1$, reject $H_0$ if $C > c_\alpha$ or $C^* > z_\alpha$
- $H_1: \gamma^2 < 1$, reject $H_0$ if $C\leq c_{1-\alpha}$ or $C^* \leq -z_\alpha$
- $H_1: \gamma^2 \neq 1$: reject $H_0$ if ($C_\alpha\geq c_{\alpha_1}\text{ or } c_{1-\alpha_2}-1$) or ($|C^*|\geq z_{\alpha/2}$)

## Test Statistic
### Procedure
1. Combine the samples
2. Give the samllest and the largest observations rank 1
3. Give the second smallest and largest observations rank 2
4. and so on.

### Test Statistic
$$C=\sum_{j=1}^{n} R_{j}$$
where $R_j$ denote the score assigned to $Y_j$

### Exact Distribution
There are $\binom{N}{n}$ possible "meshings" of $X$'s and $Y$'s.
- If $N$ is even, $E_{0}(C)=\frac{n(N+2)}{4}, \quad \operatorname{Var}_{0}(C)=\frac{m n(N+2)(N-2)}{48(N-1)}$
- If $N$ is odd, $E_{0}(C)=\frac{n(N+1)^{2}}{4 N}, \quad \operatorname{Var}_{0}(C)=\frac{m n(N+1)\left(3+N^{2}\right)}{48 N^{2}}$

## Large Sample Approximation
$$C^{*}=\frac{C-E_{0}(C)}{\sqrt{\operatorname{Var} 0}(C)} \sim N(0,1)$$

## Tie

- If $N$ is even 
$$E_{0}(C)=\frac{N+2}{4}\quad\operatorname{Var}_{0}(C)=\frac{m n\left[16 \sum_{j=1}^{g} t_{j} r_{j}^{2}-N(N+2)^{2}\right]}{16 N(N-1)}$$
- If $N$ is odd
$$E_{0}(C)=\frac{n(N+1)^{2}}{4 N}\quad\operatorname{Var}_{0}(C)=\frac{m n\left[16 N \sum_{j=1}^{g} t_{j} r_{j}^{2}-(N+1)^{4}\right]}{16 N^{2}(N-1)}$$
