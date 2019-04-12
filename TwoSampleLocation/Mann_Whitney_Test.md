# Mann-Whitney Test

## Hypothesis
$$H_0: \Delta=0$$

## Test Statistics

$$U=\sum_{i=1}^{m} \sum_{j=1}^{n} \phi\left(X_{i}, Y_{j}\right)$$
where $\phi\left(X_{i}, Y_{j}\right)=\left\{\begin{array}{ll}{1} & {\text { if } X_{i}<Y_{j}} \\ {0} & {\text { otherwise }}\end{array}\right.$

- $U=\text { no. of pairs with } X_{i}<Y_{j}$
- $U=W-\frac{n(n+1)}{2}$
- $E_{0}(U)=\frac{m n}{2}$
- $\operatorname{Var}_{0}(U)=\frac{m n(m+n+1)}{12}$

## Tie
$$U=\sum_{i=1}^{m} \sum_{j=1}^{n} \phi^{*}\left(X_{i}, Y_{j}\right)$$
$$\phi^{*}\left(X_{i}, Y_{j}\right)=\left\{\begin{array}{cl}{1} & {\text { if } X_{i}<Y_{j}} \\ {\frac{1}{2}} & {\text { if } X_{i}=Y_{j}} \\ {0} & {\text { otherwise }}\end{array}\right.$$