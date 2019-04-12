# Lepage Test

## Hypothesis

$$H_0: F(t) = G(t)\text{ for every }t\quad H_1:\theta_1\neq\theta_2\text{ and/or }\eta_{1}\neq\eta_{2}$$
- Under the location-scale parameter model $H_1: \theta_1=\theta_2\text{ and }\eta_{1}=\eta_{2}$

## Test Statistic
$$D=\frac{\left[W-E_{0}(W)\right]^{2}}{\operatorname{Var}_{0}(W)}+\frac{\left[C-E_{0}(C)\right]^{2}}{\operatorname{Var}_{0}(C)}$$
where $W=\sum_{j=1}^nS_j$ is the Wilcoxon rank sum statistic, $C=\sum_{j=1}^nR_j$ is the test statistic of Ansari-Bradley test.
- Reject $H_0$ if $D\geq d_\alpha$

## Large Sample Approximation
Under $H_0$, as $m, n \rightarrow \infty$
$$D \sim \chi_{2}^{2}$$
Reject $H_0$ if $D\geq \chi_{2, \alpha}^{2}$

## Tie
$$W\Rightarrow W^*\quad C\Rightarrow C^*$$