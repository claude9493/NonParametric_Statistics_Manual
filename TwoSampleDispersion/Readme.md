# Two Sample Dispersion Problem
- [Ansari-Bradley Test][1]
- [Siegel Tukey Test][2]
- [Lepage Test][3]
- [Kolmogorov-Smirnov Test][4]

## Data

Two indenpendent random samples. One sample from each of two underlying populations.

$N=m+n$ observations $X_1,\dots,X_m$ and $Y_1,\dots,Y_n$

## Assumptions
**A1.** $X_1,\dots,X_m$ and $Y_1,\dots,Y_n$ are random samples from continuous population 1 and 2. $X$'s are i.i.d, $Y$'s are i.i.d (independence within each sample)<br>
**A2.** $X$'s and $Y$'s are mutually independent (independence between the two samples). 

## Hypothesis

$$H_{0} : F(t)=G(t) \text { for every } t$$

$X \sim F(x), Y \sim G(y)$

- The $Y$ population has the same general form as the $X$ population, but they could have different medians and scale parameters.
  - location scale parameter model:  $$F(t)=H\left(\frac{t-\theta_{1}}{\eta_{1}}\right) \text { and } G(t)=H\left(\frac{t-\theta_{2}}{\eta_{2}}\right),-\infty< t<\infty$$
  - $\frac{X-\theta_{1}}{\eta_{1}} \stackrel{d}{=} \frac{Y-\theta_{2}}{\eta_{2}}$
- Tripical alternative hypothesis: $H_1:$ $Y$ population has a greater (or less) variability associated with it than does the $X$ population.


[1]: .\TwoSampleDispersion\Ansari_Bradley_Test.md "Ansari-Bradley Test"
[2]: .\TwoSampleDispersion\Siegel_Tukey_Test.md "Siegal Tukey Test" 
[3]: .\TwoSampleDispersion\Lepage_Test.md "Lepage Test" 
[4]: .\TwoSampleDispersion\Kolmogorov_Smirnov_Test.md "Kolmogorov-Smirnov Test"