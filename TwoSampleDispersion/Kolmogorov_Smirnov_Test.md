# Kolmogorov-Smirnov Test
## Hypothesis
$$H_0: F(t)=G(t)\text{ for every }t\quad H_1: F(t)\neq G(t)\text{ for at least one }t$$

## Test Statistic
$$J=\frac{m n}{d} \max _{-\infty<t<\infty}\left\{\left|F_{m}(t)-G_{n}(t)\right|\right\}$$
where $F_{m}(t)=\frac{1}{m} \sum_{i=1}^{m} I\left\{X_{i} \leq t\right\}, \quad G_{n}(t)=\frac{1}{n} \sum_{j=1}^{n} I\left\{Y_{j} \leq t\right\}$ and $d$ is the greatest common divisor of $m$ and $n$
- $J=\frac{m n}{d} \max _{i=1, \ldots, N}\left\{\left|F_{m}\left(Z_{(i)}\right)-G_{n}\left(Z_{(i)}\right)\right|\right\}$
  - $Z_{(1)} \leq \ldots \leq Z_{(N)}$ is the $N$ ordered values of the combined samples
- Reject $H_0$ if $J\geq j_\alpha$

### Exact Distribution
Under $H_0$ there are $\binom{N}{n}$ possible meshings of the $X$'s and $Y$'s.

## Large Sample Approximation
$$J^{*}=\left(\frac{m n}{N}\right)^{1 / 2} \max _{i=1, \ldots, N}\left\{\left|F_{m}\left(Z_{(i)}\right)-G_{n}\left(Z_{(i)}\right)\right|\right\}=\frac{d}{(m n N)^{1 / 2}} J$$

As min($m, n$)$\rightarrow\infty$,
$$F(s)=P_{0}\left(J^{*}<s\right) \rightarrow \left\{\begin{array}{cc}{\sum_{k=-\infty}^{\infty}(-1)^{k} e^{-2 k^{2} s^{2}}} & {s>0} \\ {0} & {s \leq 0}\end{array}\right.$$
Defing the function $Q(s)$ by
$$Q(s)=1-\sum_{k=-\infty}^{\infty}(-1)^{k} e^{-2 k^{2} s^{2}}, s>0$$
Reject $H_0$ if $J^*\geq q_\alpha^*$, where $Q(q_\alpha^*)=\alpha$
    
    qKolSmirnLSA(alpha)

## One Sample K-S Test (Goodness of Fit)
### Hypothesis
$$H_{0} : F(t)=F_{0}(t), \quad H_{1} : F(t) \neq F_{0}(t)$$

### Test Statistic
$$D_{n}=\sup _{t}\left|\hat{F}_{n}(t)-F_{0}(t)\right|$$

Let $X_{(1)},\dots,X_{(n)}$ be the order statistic, $D_n$ can be computed from 
$$D_{n}=\max _{i}\left\{\max \left[\hat{F}_{n}\left(X_{(i)}\right)-F_{0}\left(X_{(i)}\right), F_{0}\left(X_{(i)}\right)-\hat{F}_{n}\left(X_{(i-1)}\right)\right]\right\}$$
where $\hat{F}_{n}\left(X_{(i)}\right)=\frac{i}{n}, \hat{F}_{n}\left(X_{(i-1)}\right)=\frac{i-1}{n}$

### Large Sample Approximation
$$\lim _{n \rightarrow \infty} P\left(D_{n} \geq \frac{z}{\sqrt{n}}\right)=L(z)$$
where $L(z)=1- 2\sum_{i=1}^{\infty}(-1)^{i-1} e^{-2 i^{2} z^{2}}$

### Recap: Goodness of Fit Test
To test whether the data follow a specific distribution.
#### Procedure
1. Partition the sample sapce into $m$ disjoint bins.
2. $O_i$ is the number of observations that fall in the $i$th Bin. $E_i$ is the expected frequency in $i$th Bin. $E_{i}=n * P\left(X \in \operatorname{Bin} i | H_{0}\right)$, $n$ is the sample size.
#### Test Statistic
$$\chi^{2}=\sum_{i=1}^{m} \frac{\left(O_{i}-E_{i}\right)^{2}}{E_{i}} \sim \chi_{m-1-k}^{2}$$
where $k$ is the number of parameters in the distribution $F_0$