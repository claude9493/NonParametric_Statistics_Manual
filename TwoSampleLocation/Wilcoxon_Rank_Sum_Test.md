# Wilcoxon Rank Sum Test

## Hypothesis
$$H_0: \Delta=0$$

- $H_1: \Delta>0$, reject $H_0$ if $W\geq w_\alpha$ or $W^*\geq z_\alpha$
- $H_1: \Delta < 0$, reject $H_0$ if $W\leq n(m+n+1)-w_\alpha$ or $W^*\leq-z_\alpha$
- $H_1: \Delta\neq0$, reject $H_0$ if $W \geq w_{\alpha / 2} \text { or if } W \leq n(m+n+1)-w_{\alpha / 2}$  OR $|W^*|\geq z_{\alpha/2}$

## Test Statistics
$$W=\sum_{j=1}^{n} S_{j}$$
where $S_j$ is the rank of $Y_j$ in the combined sample

### Exact Distribution
$\binom{N}{n}$ possible sets of the rank for the $Y$'s. Under $H_0$, every set is equally likely.

- $$\min W=\frac{n(n+1)}{2},\quad\max W=\frac{n(N+m+1)}{2}$$
- $$E_{0}(W)=\frac{n(N+1)}{2},\quad\operatorname{Var}_{0}(W)=\frac{n m(N+1)}{12}$$
- When $H_0$ is true, the distribution of $W$ is symmetric about its mean.

## Large Sample Approximation
$$W^{*}=\frac{W-E_{0}(W)}{\sqrt{\operatorname{Var}_0(W)}} \sim N(0,1)$$

## Ties
Average the ranks of tied observations.

- $\operatorname{Var}_{0}(W)=\frac{n m(N+1)}{12}-\frac{m n}{12 N(N-1)} \sum_{j=1}^{g}\left(t_{j}-1\right) t_{j}\left(t_{j}+1\right)$
- $W^{*}=\frac{W-E_{0}(W)}{\sqrt{\operatorname{Var}_{0}(W)}} \sim N(0,1)$

## Estimator
Suppose $X \stackrel{d}{=} Y-\Delta$.

$$\hat{\Delta}=\operatorname{median} \text { of }\left(Y_{j}-X_{i}\right)$$
- $\hat{\Delta}=a$ such that there are as many $X$ larger than $Y-a$ as are smaller than $Y-a$
- $U=$ no.of $\left(X_{i}, Y_{j}-a\right)$ s.t. $X_{i}<Y_{j}-a =\sum_{i=1}^{m} \sum_{j=1}^{n} I\left(X_{i}, Y_{j}-a\right) \approx \frac{m n}{2}$
  - $\hat{\Delta}=a=\left\{\begin{array}{cc}{U^{(k+1)}} & {m n=2 k+1} \\ {\frac{U^{(k)}+U^{(k+1)}}{2}} & {m n=2 k}\end{array}\right.$

## Confidence Interval

$$\left(U^{\left(C_{\alpha}\right)}, U^{\left(m n+1-C_{\alpha}\right)}\right)$$

where $C_{\alpha}=\frac{n(2 m+n+1)}{2}+1-w_{\alpha / 2}$ and $w_{\alpha / 2}$  denote the upper $\alpha/2$ percentile point of the null distribution of $W$ 

- $U^{(1)} \leq \cdots U^{(m n)}$ are the ordered statistics of $Y-X$
- $C_{\alpha} \approx \frac{m n}{2}-z_{\alpha / 2} \sqrt{\frac{m n(m+n+1)}{12}}$