# Two-Sample Location Problem
- [Wilcoxon Rank Sum Test][1]
- [Mann-Whitney Test][2]
- [Fligner-Policello Test][3]

## Data
$N=m+n$ observations $X_1,\dots,X_m$ and $Y_1,\dots,Y_n$, $n\leq m$

## Assumptions
**A1.** $X$'s are iid random sample from population 1, $Y$'s are iid random sample from populaiton 2. <br>
**A2.** $X$'s and $Y$'s are mutually independent <br>
**A3.** Populations 1 and 2 are continuous polulations

## Hypothesis
$H_0:$ $X^{\prime} s \& Y^{\prime} s$ come from the sample population

$H_1:$ There is a location shift

- Let $F$ and $G$ be the distribution functions corresponding to the two populations. <br> $$H_0: F(t)=G(t), \text{for every } t$$
- Location-Shift Model: $G(t)=F(t-\Delta)$ for every $t$
  - $Y\overset{d}{=}X+\Delta$
  - If $E(X)$ exists, $\Delta=E(Y)-E(X)$
  - $H_0: \Delta=0$




[1]: .\TwoSampleLocation\Wilcoxon_Rank_Sum_Test.md "Wilcoxon Rank Sum Test"
[2]: .\TwoSampleLocation\Mann_Whitney_Test.md "Mann Whitney Test"
[3]: .\TwoSampleLocation\Fligner_Policello_Test.md "Fligner_Policello Test"