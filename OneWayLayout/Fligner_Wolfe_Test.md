# Fligner-Wolfe Test
One treatment is regarded as a control group or baseline. We are interested in assessing which, if any, of the treatments is better/worse than the control. WLOG, we label the treatments so that the control corresponds to treatment 1.

## Hypothesis
$$H_0: \tau_i=\tau_1, \text{for }i=2,\dots,k$$

- $H_4: \tau_i\geq\tau_1, \text{for }i=2,\dots,k \text{ with at least one strict inequality}$
  - Reject $H_0$ if $FW\geq f_\alpha$
  - Reject $H_0$ if $FW^*\geq z_\alpha$
- $H_5: \tau_i\leq\tau_1, \text{for }i=2,\dots,k \text{ with at least one strict inequality}$
  - Reject $H_0$ if $FW\leq N^*(N+1)-f_\alpha$
  - Reject $H_0$ if $FW^*\leq-z_\alpha$

where $N^{*}=\sum_{j=2}^{2} n_{j}$
## Test Statistic
$$FW= \sum_{j=2}^{k} \sum_{i=1}^{n_{j}} r_{i j}$$
The statistic $FW$ can be viewed as a two-sample [Wilcoxon rank sum statistic][1], with sample size $m=n_1$ and $n=N^*$
### Exact Distribution
$$E_{0}(F W)=\frac{N^{*}(N+1)}{2}$$
$$\operatorname{Var}_{0}(F W)=\frac{n_{1} N^{*}(N+1)}{12}$$

## Large Sample Approximation
As $\min \left(n_{1}, N^{*}\right) \rightarrow \infty$,
$$F W^{*}=\frac{F W-E_{0}(F W)}{\sqrt{\operatorname{Var}_{0}(F W)}} \sim N(0,1)$$


## Tie
$$E_{0}(F W)=\frac{N^{*}(N+1)}{2}$$
$$\operatorname{Var}_{0}(F W)=\frac{n_{1} N^{*}}{12}\left[N+1-\frac{\sum_{j=1}^{g} t_{j}\left(t_{j}-1\right)\left(t_{j}+1\right)}{N(N-1)}\right]$$

[1]: .\TwoSampleLocation\Wilcoxon_Rank_Sum_Test.md "Wilcoxon Rank Sum Test"