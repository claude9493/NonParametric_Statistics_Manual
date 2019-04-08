# Binomial Test
The data consists of n independent repeated Bernoulli trials having constant probability of success p. On the basis of these outcomes, we wish to make inferences about p.

## Assumptions
**A1.** The outcome of each trial can be classified as a success or a failure.<br>
**A2.** The probability of a success, denoted by $p$, remains constant from trial to trial<br>
**A3.** The $n$ trials are independent
## Null Hypothesis
$$H_0: p = p_0$$

## Test Statistics
$$B = \text{number of successes}$$

$E_{p_{0}}(B) =n p_{0},\quad \operatorname{var}_{p_{0}}(B) =n p_{0}\left(1-p_{0}\right)$

Under $H_0$, $B\sim\text{Bino}(n, p_0)$.

### Large Sample Approximation
$$B^{*}=\frac{B-E_{p 0}(B)}{\left\{\operatorname{var}_{p_{0}}(B)\right\}^{1 / 2}}=\frac{B-n p_{0}}{\left\{n p_{0}\left(1-p_{0}\right)\right\}^{1 / 2}}$$
When $H_{0}$ is true, $B^{*}$ has, as $n$ tends to infinity, an asymptotic $N(0,1)$
distribution.

## Alternative Hypothesis and Reject Rule
### One-Sided Upper-Tile  Test
$$H_1: p > p_0$$
 Reject $H_0$ if $B \geq b_\alpha$
### One-Sided Lower-Tile Test
$$H_1: p < p_0$$
Reject $H_0$ if $B \leq c_\alpha$
### Two-Sided Test
$$H_1: p \neq p_0$$
Reject $H_0$ if $B \geq b_{\alpha_1}$ or $B \leq c_{\alpha_2}$, where $\alpha_1+\alpha_2 = 1$
