# Wilcoxon Signed Rank Test

## Hypothesis
$$H_0: \theta = 0$$

- For $H_1: \theta>0$, reject $H_0$ if $T^+\geq t_\alpha$ or $T^*\geq z_\alpha$
- For $H_{1} : \theta<0,$ reject $H_{0}$ if $T^{+} \leq \frac{n(n+1)}{2}-t_{\alpha} .$ or $T^*\leq -z_\alpha$ 
- For $H_{1} : \theta \neq 0,$ reject $H_{0}$ if $T^{+} \geq t_{\alpha / 2}, T^{+} \leq \frac{n(n+1)}{2}-t_{\alpha / 2}$ or $|T^*|\geq z_{\alpha/2}$

## Test Statistics

$$T^+=\sum_{i=1}^nR_i\psi_i$$

$T^+$ is the sum of positive signed ranks.
$R_i$ is the rank of the absolute difference(data) $|Z_1|,|Z_2|,\dots,|Z_n|$
, $\psi_i=I(Z_i>0)$

### Exact Distribution
$2^n$ possible sets of signed ranks are equally likely. Calculate $T^+$ for each of the $2^n$ combinations and get the exact distribution.

$$\min \left(T^{+}\right)=0 \text{ and } \max \left(T^{+}\right)=\frac{n(n+1)}{2}$$

$$E_{0}\left(T^{+}\right)=\frac{n(n+1)}{4},\quad\operatorname{Var}_{0}\left(T^{+}\right)=\frac{n(n+1)(2 n+1)}{24}$$

## Large Sample Approximation

$$T^{*}=\frac{T^{+}-E\left(T^{+}\right)}{\sqrt{\operatorname{Var}\left(T^{*}\right)}} \sim N(0,1)$$


## Ties

Discard the zero values among $Z$'s and redefnie $n$ to the number of **nonzero** $Z$'s.

If there are ties among the $|Z$'s, assign each of the observations in a tied group the average of the integer ranks that are asosciated with the tied group.

- $\operatorname{Var}_{0}\left(T^{+}\right)=\frac{n(n+1)(2 n+1)}{24}-\frac{1}{48} \sum_{i=1}^{g} t_{j}\left(t_{j}-1\right)\left(t_{j}+1\right)$
  - where $g$ denotes the number of tied groups of nonzero $|Z|^{\prime} s, t_{j}$ is the size of
the tied group $j .$ No ties: $g=n, t_{j}=1$

## Estimator

$$\hat{\theta}=\left\{\begin{array}{cc}{W^{(k+1)}} & {M=2 k+1} \\ {\frac{W^{(k)}+W^{(k+1)}}{2}} & {M=2 k}\end{array}\right.$$

- Walsh average: $\left\{\frac{Z_{i}+Z_{j}}{2}, i \leq j .\right\}$
- $W^{(1)} \leq W^{(2)} \leq \cdots \leq W^{(M)},$ where $M=\frac{n(n+1)}{2},$ denote the ordered values
of $\left(Z_{i}+Z_{i}\right) / 2$.


## Confidence Interval
$$\left(W^{\left(c_{\alpha}\right)}, W^{\left(M+1-c_{\alpha}\right)}\right)$$

where 
$$c_{\alpha}=\frac{n(n+1)}{2}+1-t_{\alpha / 2}$$

### Large Sample Approximation
$$c_{\alpha} \approx \frac{n(n+1)}{4}-z_{\alpha / 2} \sqrt{\frac{n(n+1)(2 n+1)}{24}}$$