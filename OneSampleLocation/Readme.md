# One-Sample Location Problem
- [Sign Test][1]
- [Wilcoxon Signed Rank Test][2]

## Data
$n$ observations $Z_1,\dots,Z_n$


## Assumptions
**A1.** $Z_1,\ldots,Z_n$ are mutually independent. <br>
**A2.** Each $Z$ comes from the same continuous populaiton with median $\theta$, so that $P(Z_i > \theta) = P(Z_i < \theta) = 1/2,i=1,2,\dots,n$

## Hypothesis
$H_0: \theta=\theta_0$

- Without generality, let $\theta_0=0$. If not, denote$Z_i' = Z_i-\theta$

<!-- 
Each $Z_i, i=1, \ldots, n,$ comes from a continuous population (not necessarily the
same one) that is symmetric about a common median $\theta .$ If $F_{i}$ represents the
distribution function for $Z_{i}, i=1, \ldots n,$ this assumption requires that $F_{i}(\theta+t)+F_{i}(\theta-t)=1,$ for every $t$ and $i=1, \ldots, n$. The parameter $\theta$ is referred to as the treatment effect.
 -->

[1]: .\Sign_Test.md "Sign Test"
[2]: .\Wilcoxon_Signed_Rank_Test.md "Wilcoxon Signed Rank Test"