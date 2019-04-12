# Siegel-Tukey Test

## Hypothesis

## Test Statistics
### Procedure
1. Combine the samples.
2. Give the smallest observation rank 1.
3. Give the largest observation rank 2.
4. Give the next largest observation rank 3.
5. Give the next smallest observation rank 4.
6. and so on
### Test Statistic
$$W_s = \text{ sum of } Y\text{'s rank}$$
- Under $H_0$, we would expect the sum of ranks(adjusted for sample size) to be about the same for each group
- If $X$ is more variable, $W_s$ would tend to be large.
### Exact Distribution
Under $H_0$ the distribution of $W_s$ is exactly the same as the distirbutio of $W$ statistic in Wilcoxon Rank Sum test.