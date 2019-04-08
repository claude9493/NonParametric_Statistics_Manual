# Manual of Non-Parametric Statistics
-----
> A manual/documentation of non-parametric statistics

## What it is
-----
In this manual, several non-parametric statistics methods are described in detailed, including when to use, under what circumstances, how to use, and some other aspects.

## Instruction
-----
Each folder includes some non-parametric tests for the problem specified by the folder's name. In each file, the test statistics, rejection region, large smaple approximation and some other points are provided, details of the structure of single file are in [Structure](#struc).

## Contents
-----
- [x] [One-Sample Location Problem][1]
  - [x] [Sign Test][2]
  - [x] [Wilcoxon Signed Rank Test][3]
- [x] [Two-Sample Location Problem][4]
  - [ ] Wilcoxon Rank Sum Test
  - [ ] Mann-Whitney Test
  - [ ] Fligner-Policello Test
- [ ] Two-Sample Dispersion Problem
  - [ ] Ansari-Bradley Test
  - [ ] Siegel Tukey Test
  - [ ] Lepage Test
  - [ ] Kolmogorov-Smirnov Test

## <span id="struc">Structure</span>
-----
- Hypothesis $H_0$, several $H_1$
- Test Statistics (with explanation and its $\text{E}_0$ and $\text{Var}_0$)
- Rejection Region (for different $H_1$)
- Large Sample Approximation (Statistics and how to use)
- Tie
- Estimator
- Confidence Interval

[1]: .\OneSampleLocation\Readme.md "One Sample Location Problem"
[2]: .\OneSampleLocation\Sign_Test.md
[3]: .\OneSampleLocation\Wilcoxon_Signed_Rank_Test.md
[4]: .\TwoSampleLocation\Readme.md "Two Sample Location Problem"
[5]: .\TwoSampleLocation\Wilcoxon_Rank_Sum_Test.md

