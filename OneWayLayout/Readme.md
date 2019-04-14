# One-Way Layout
- [Kruskal Wallis Test][1]
- [Jonckheere-Terpstra Test][2]
- [Mack-Wolfe Test][3]
- [Fligner-Wolfe Test][4]
- [Dwass-Steel-Critchlow-Fligner Test][5]
## Data
There are $k$ treatments/groups of sample and $N=\sum_{j=1}^kn_j$ observations in total, with $n_j$ observations from the $j$th treatment.

![Data](..\Figures\One_Way_Layout_Data.png)

## Assumptions
- The $N$ random variables are mutually independent.
- For each fixed $j\in\{1,\dots,k\}$, the $n_j$ random variables $\{X_{1j},X_{2j},\dots,X_{nj}\}$ are a random sample from a continuous distribution with distribution function $F_j$
- $F_j(t) = F(t-\tau_j),\quad -\infty<t<\infty$ for $j=1,\dots,k$

Under these assumptions:
$$X_{i j}=\theta+\tau_{j}+e_{i j}, \quad i=1, \dots, n_{j} ; j=1, \ldots, k$$
- $\theta$ : over all median
- $\tau_j$ : treatment $j$ effect
- The $N$ $e$'s form a random sample from a continuous distribution with median 0

## Hypothesis
Null hypothesis: no differences among the treatment effects $\tau_1,\dots,\tau_k$
$$H_0: \tau_1=\dots=\tau_k$$

- Equivalent: $H_0: F_1=F_2=\dots=F_k=F$

Alternative hypothesis varies in tests.
- $H_1: \tau_1,\dots,\tau_k\text{ not all equal}$ - [Kruskal Wallis Test][1]
- $H_2 : \tau_{1} \leq \tau_{2} \leq \cdots \leq \tau_{k}\text{ with at least one strict inequality}$ - [Jonckheere-Terpstra Test][2]
- $H_3 : \tau_{1} \leq \tau_{2} \leq \cdots \leq \tau_{p-1} \leq \tau_{p} \geq \tau_{p+1} \geq \cdots \geq \tau_{k}\text{ with at least one strict inequality}$ - [Mack-Wolfe Test][3]
- $H_4: \tau_i\geq\tau_1, \text{for }i=2,\dots,k \text{ with at least one strict inequality}$ - [Fligner-Wolfe Test][4]
- $H_5: \tau_i\leq\tau_1, \text{for }i=2,\dots,k \text{ with at least one strict inequality}$ - [Fligner-Wolfe Test][4]


[1]: ./OneWayLayout/Kruskal_Wallis_Test.md "Kruskal Wallis Test"
[2]: ./OneWayLayout/Jonckheere_Terpstra_Test.md "Jonckheere-Terpstra Test"
[3]: ./OneWayLayout/Mack_Wolfe_Test.md "Mack-Wolfe Test"
[4]: ./OneWayLayout/Fligner_Wolfe_Test.md "Fligner-Wolfe Test"
[5]: ./OneWayLayout/Dwass_Steel_Critchlow_Fligner_Test.md "Dwass-Steel-Critchlow-Fligner Test"