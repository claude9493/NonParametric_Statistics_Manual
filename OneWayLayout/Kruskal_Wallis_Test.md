# Kruskal Wallis Test
## Hypothesis
$$H_0: \tau_1=\dots=\tau_k$$
$$H_1: \tau_1,\dots,\tau_k\text{ not all equal}$$

- Reject $H_0$ if $H\geq h_\alpha$
## Test Satistic
### Procedure
1. Combine all $N$ observations from $k$ samples
2. Rank the combined sample of $N$ observations
3. Let $r_{ij}$ denote the rank of $X_{ij}$, set $R_j=\sum_{i=1}^{n_j}r_{ij}$ and $R_{ . j}=\frac{R j}{n_{j}}, j=1, \dots, k$

Under $H_0$, $R^{*}=\left(r_{11}, \ldots, r_{n_{1} 1}, r_{22}, \dots, r_{n_{2} 2}, \dots, r_{1 k}, \dots, r_{n_{k} k}\right)$ uniformly distribute over all $N!$ permutations of $(1,2,\dots,N)$
- $E_{0}\left(r_{i j}\right)=\sum_{i=1}^{N} i * \frac{(N-1) !}{N !}=\frac{N+1}{2}$
 - $E_{0}\left(R_{ . j}\right)=\frac{1}{n_{j}} \sum_{i=1}^{n_{j}} E_{0}\left(r_{i j}\right)=\frac{N+1}{2}$

### Test Statistic
$$H=\frac{12}{N(N+1)} \sum_{j=1}^{k} n_{j}\left(R_{ . j}-\frac{N+1}{2}\right)^{2}=\left(\frac{12}{N(N+1)} \sum_{j=1}^{k} \frac{R_{j}^{2}}{n_{j}}\right)-3(N+1)$$

- $D=\sum_{j=1}^{k} n_{j}\left(R_{ . j}-\overline{R}\right)^{2}=\sum_{j=1}^{k} n_{j}\left(R_{ . j}-\frac{N+1}{2}\right)^{2}$ is a measure of discrepancy, similar to the sum of squares $SSB = \sum_{j=1}^{k} n_{j}\left(\bar{X}_{ . j}-\bar{X}\right)^{2}$ in one-way ANOVA.
  - $H=\frac{12}{N(N+1)} D$, the factor $\frac{12}{N(N+1)}$ makes the distribuion more like $\chi^2$ in large sample.


## Large Sample Approximation
As min($n_1,\dots,n_k$)$\rightarrow\infty$ ($>3$)
$$H \sim \chi_{k-1}^{2}$$
Reject $H_0$ if $H \geq \chi_{k-1, \alpha}^{2}$
- $k=2$: two-sided Wilcoxon rank sum test, $H=\frac{[W-E(W)]^{2}}{\operatorname{Var}(W)}$

## Tie
Assign each of the observations in a tied group the average of the interge ranks.

$$H^{\prime}=\frac{H}{1-\left(\sum_{j=1}^{g}\left(t_{j}^{3}-t_{j}\right) /\left[N^{3}-N\right]\right)}$$