# Dwass-Steel-Critchlow-Fligner Test

A multiple comparsion based on pairwise two-sample rankings that is designed to make decisions about individual differences between pairs of treatment effects $(\tau_i, \tau_j)$ for $i<j$, in a setting where general alternatives [$H_1$](./OneWayLayout/Readme.md) are of interest.  Procedure of this test would generally be applied to one-way layout data after rejection [$H_0$](./OneWayLayout/Readme.md) with [Kruskal-Wallis Test](./OneWayLayout/Kruskal_Wallis_Test.md)

In this setting, it is important to reach conclusions about all $\binom{k}{2}=k(k-1)/2$ pairs of treatment effects, and those conclusions are natually two-sided in nature.

## Test Statistic
For each pair of treatment $(i,j)$, let
$$W_{i j}=\sum_{b=1}^{n_{j}} R_{i b}$$
$$W_{i j}^{*}=\sqrt{2}\left[\frac{W_{i j}-E_{0}\left(W_{i j}\right)}{\left\{\operatorname{var}_{0}\left(W_{i j}\right)\right\}^{1 / 2}}\right]=\frac{W_{i j}-\frac{n_{j}\left(n_{i}+n_{j}+1\right)}{2}}{\left\{n_{i} n_{j}\left(n_{i}+n_{j}+1\right) / 24\right\}^{1 / 2}}$$
$\text { for } 1 \leq i<j \leq k$

where $R_{i 1}, \dots, R_{i n_{j}} \text { are the ranks of } X_{1 j}, \dots, X_{n_{j} j}$, respectively, among the combined $i$th and $j$th samples.

Decide $\tau_{u} \neq \tau_{v} \text { if }\left|W_{u v}^{*}\right| \geq w_{\alpha}^{*}$, where $w_\alpha^*$ is chosen to make the experimentwise error rate equal to $\alpha$
$$P_{0}\left(\left|W_{u v}^{*}\right|<w_{\alpha}^{*}, u=1, \ldots, k-1 ; v=u+1, \ldots, k\right)=1-\alpha$$

### Critical Value $w_\alpha^*$
Under $H_0$,
$$P_{0}\left(\left|W_{uv}^{*}\right|<c, \text { for all } u<v\right)=\frac{\#\left\{W_{u v}^{*} |<c, \text { for all } u<v\right\}}{N ! / \prod_{j=1}^{k} n_{j} !}$$

    cSDCFlig(alpha, n)

## Large Sample Approximation
As $\min(n_1,\dots,n_k)\rightarrow\infty$
$$\tau_{u} \neq \tau_{v} \text { if }\left|W_{u v}^{*}\right| \geq q_{\alpha}$$
where $q_\alpha$ is the upper $\alpha$th percentile point for the distribution of the range of $k$ independent $N(0,1)$ variables.
    
    cRangekNormal(alpha, k)

## Tie
$$\frac{\operatorname{var}_{0}\left(W_{i j}\right)}{2}=\frac{n_{i} n_{j}}{24}\left[n_{i}+n_{j}+1-\frac{\sum_{b=1}^{g_{i j}}\left(t_{b}-1\right) t_{b}\left(t_{b}+1\right)}{\left(n_{i}+n_{j}\right)\left(n_{i}+n_{j}-1\right)}\right]$$