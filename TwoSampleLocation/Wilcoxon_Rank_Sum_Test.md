# Wilcoxon Rank Sum Test

## Hypothesis
$H_0: \Delta=0$

- $H_1: \Delta>0$, reject $H_0$ if $W\geq w_\alpha$
- $H_1: \Delta < 0$, reject $H_0$ if $W\leq n(m+n+1)-w_\alpha$

## Test Statistics
$$W=\sum_{j=1}^{n} S_{j}$$
where $S_j$ is the rank of $Y_j$ in the combined sample

### Exact Distribution
$\left( \begin{array}{l}{N} \\ {n}\end{array}\right)$ possible sets of the rank for the $Y$'s. Under $H_0$, every set is equally likely.

- $$\min W=\frac{n(n+1)}{2},\quad\max W=\frac{n(N+m+1)}{2}$$
- $$E_{0}(W)=\frac{n(N+1)}{2},\quad\operatorname{Var}_{0}(W)=\frac{n m(N+1)}{12}$$
- When $H_0$ is true, the distribution of $W$ is symmetric about its mean.

## Large Sample Approximation
$$W^{*}=\frac{W-E_{0}(W)}{\sqrt{\operatorname{Var}_0(W)}} \sim N(0,1)$$

## Ties
Average the ranks of tied observations.

- $\operatorname{Var}_{0}(W)=\frac{n m(N+1)}{12}-\frac{m n}{12 N(N-1)} \sum_{j=1}^{g}\left(t_{j}-1\right) t_{j}\left(t_{j}+1\right)$
- $W^{*}=\frac{W-E_{0}(W)}{\sqrt{\operatorname{Var}_{0}(W)}} \sim N(0,1)$