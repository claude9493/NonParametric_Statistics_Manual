# Fligner Policello Test

## Behrens-Fisher Problem
Test $H_0': \theta_x = \theta_y$ without assuming equal variances.

## Hypothesis
![](..\Figures\FiligPoliHypo.png)
## Test Statistics

$$\widehat{U}=\frac{\sum_{j=1}^{n} Q_{j}-\sum_{i=1}^{m} P_{i}}{2\left(V_{1}+V_{2}+\bar{P} \bar{Q}\right)^{1 / 2}}$$
Where
$P_{i}=[$ number of sample $Y$ observations less than $X_{i}], i=1,\dots,m$, $Q_{j}=[$ number of sample $X$ observations less than $Y_{j}], j=1,\dots,n$

We call $P_{i}$ and $Q_{j}$ the placements of $X_{i}$ and $Y_{j},$ respectively.

$\bar{P}=\frac{1}{m} \sum_{i=1}^{m} P_{i}=$ average $X$ sample placement, $\bar{Q}=\frac{1}{n} \sum_{j=1}^{n} Q_{j}=$ average $Y$ sample placement, $V_{1}=\sum_{i=1}^{m}\left(P_{i}-\bar{P}\right)^{2}$ and $V_{2}=\sum_{j=1}^{n}\left(Q_{j}-\bar{Q}\right)^{2}$

- $\widehat{U}=\frac{n^{1 / 2}\left\{(U / m n)-\frac{1}{2}\right\}}{\widehat{\sigma}}$
  - where  $\widehat{\sigma}^{2}=\frac{\sum_{j=1}^{n}\left(Q_{j}-\overline{Q}\right)^{2}+\sum_{i=1}^{m}\left(P_{i}-\overline{P}\right)^{2}+\overline{P Q}}{m^{2} n}$
## Large Sample Approximation
As $\min(m,n)\rightarrow\infty$
$$\hat{U}\sim N(0,1)$$
Replace $u$ with $z$ in section hypothesis to get the rejectoin rule.

## Tie

$P_{i}=\left\{\left[\text { number of sample } Y \text { observations less than } X_{i}\right]\right.+\frac{1}{2}\left[\text { number of sample } Y \text { observations equal to } X_{i}\right] \}$


