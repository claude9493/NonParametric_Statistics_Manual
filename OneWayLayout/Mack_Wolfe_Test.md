# Mack-Wolfe Test
## Hypothesis
Let $p\in\{1,2,\dots,k\}$ be a fixed treatment label, we consider the umbrella alternative hypothesis:
$$H_3 : \tau_{1} \leq \tau_{2} \leq \cdots \leq \tau_{p-1} \leq \tau_{p} \geq \tau_{p+1} \geq \cdots \geq \tau_{k}\text{ with at least one strict inequality}$$
- The umbrella is said to have a peak at population $p$
- Jonckheere-Terpstra Test's alternative is simply a special case of umbrella alternative with peak at $p=k$
  
## Test Statistic
If $p$ is known, the peak-known umbrella statistic is 
$$A_{p}=J_{up}+J_{down}=\sum_{u=1}^{v-1} \sum_{v=2}^{p} U_{u v}+\sum_{u=p}^{v-1} \sum_{v=p+1}^{k} U_{v u}$$
Rekect $H_0$ if $A_p\geq a_{p,\alpha}$

### Exact Distribution
$$E_{0}\left(A_{p}\right)=E_{0}\left(J_{u p}\right)+E_{0}\left(J_{d o w n}\right)=\frac{1}{4}\left[N_{1}^{2}-\sum_{t=1}^{p} n_{t}^{2}\right]+\frac{1}{4}\left[N_{2}^{2}-\sum_{t=p}^{k} n_{t}^{2}\right]=\frac{1}{4}\left[N_{1}^{2}+N_{2}^{2}-\sum_{t=1}^{k} n_{t}^{2}-n_{p}^{2}\right]$$
$$\operatorname{Var}_{0}\left(A_{p}\right)=\frac{1}{72}\left[2\left(N_{1}^{3}+N_{2}^{3}\right)+3\left(N_{1}^{2}+N_{2}^{2}\right)-\sum_{i=1}^{k} n_{i}^{2}\left(2 n_{i}+3\right)-n_{p}^{2}\left(2 n_{p}+3\right)+12 n_{p} N_{1} N_{2}-12 n_{p}^{2} N \right]  $$
where $N_1=\sum_{i=1}^{p} n_{i}, N_{2}=\sum_{i=p}^{k} n_{i}, N=N_{1}+N_{2}-n_{p}$

## Large Sample Approximation
$$A_{P}^{*}=\frac{A_{p}-E_{0}\left(A_{p}\right)}{\sqrt{\operatorname{Var}_{0}\left(A_{P}\right)}} \sim N(0,1)$$
Reject $H_0$ if $A_p^*\geq z_\alpha$