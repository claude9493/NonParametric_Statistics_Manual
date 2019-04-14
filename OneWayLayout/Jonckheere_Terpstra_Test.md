# Jonckheere-Terpstra Test

## Hypothesis
A prior ordered alternatives hypothesis
$$H_2 : \tau_{1} \leq \tau_{2} \leq \cdots \leq \tau_{k}\text{ with at least one strict inequality}$$

## Test Statistic
### Procedure
Compute the $k(k-1)/2$ Mann-Whitney statistic $U_{uv}$ for any pair $1\leq u<v\leq k$
   $$U_{u v}=\sum_{i=1}^{n_{u}} \sum_{j=1}^{n_{v}} \phi\left(X_{i u}, X_{j v}\right)$$
where $\phi(a,b)=1$ if $a<b$

### Test Statistic
$$J=\sum_{u=1}^{v-1} \sum_{v=2}^{k} U_{u v}$$
Reject $H_0$ if $J\geq j_\alpha$

### Exact Distribution
Under $H_0$
$$E_{0}(J)=\sum_{u=1}^{v-1} \sum_{v=2}^{k} \frac{n_{u} n_{v}}{2}=\frac{N^{2}-\sum_{j=1}^{k} n_{j}^{2}}{4}$$
$$\operatorname{Var}(J)=\frac{N^{2}(2 N+3)-\sum_{j=1}^{k} n_{j}^{2}\left(2 n_{j}+3\right)}{72}$$

- When $k=2$, one-sided upper-tail Wilcoxon rank sum test 

## Large Sample Approximation
$$J^{*}=\frac{J-E_{0}(J)}{\sqrt{\operatorname{Var}_{0}(J)}} \sim N(0,1)$$
as min$(n_1,\dots,n_k)\rightarrow\infty$. Reject $H_0$ if $J^{*} \geq z_{\alpha}$

## Tie
$$E_{0}(J)=\frac{N^{2}-\sum_{j=1}^{k} n_{j}^{2}}{4}$$
![](..\Figures\Jonckheere_Terpstra_Tie.png)

$$
\begin{split}
\operatorname{Var}_{0}(J) \quad &= \quad \frac{1}{72}\left[N(N-1)(2 N+5)-\sum_{i=1}^{k} n_{i}\left(n_{i}-1\right)\left(2 n_{i}+5\right)-\sum_{j=1}^{g} t_{j}\left(t_{j}-1\right)\left(2 t_{j}+5\right)\right]\\
&+ \frac{1}{36 N(N-1)(N-2)}\left[\sum_{i=1}^{k} n_{i}\left(n_{i}-1\right)\left(n_{i}-2\right)\right]\left[\sum_{j=1}^{g} t_{j}\left(t_{j}-1\right)\left(t_{j}-2\right)\right]\\
&+\frac{1}{8 N(N-1)}\left[\sum_{i=1}^{k} n_{i}\left(n_{i}-1\right)\right]\left[\sum_{j=1}^{g} t_{j}\left(t_{j}-1\right)\right]
\end{split}
$$