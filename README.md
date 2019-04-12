# Manual of Non-Parametric Statistics

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
  - [x] [Wilcoxon Rank Sum Test][5]
  - [x] [Mann-Whitney Test][6]
  - [ ] [Fligner-Policello Test][7]
- [ ] [Two-Sample Dispersion Problem][8]
  - [x] [Ansari-Bradley Test][9]
  - [x] [Siegel Tukey Test][10]
  - [x] [Lepage Test][11]
  - [x] [Kolmogorov-Smirnov Test][12]
- [ ] One-Way Layout
- [ ] Two-Way Layout

## <span id="struc">Structure</span>
-----
- Hypothesis $H_0$, several $H_1$
- Test Statistics (with explanation and its $\text{E}_0$ and $\text{Var}_0$)
- Rejection Region (for different $H_1$)
- Large Sample Approximation (Statistics and how to use)
- Tie
- Estimator
- Confidence Interval

## Explanation of Some Common Variables
-----
- $N$ is always the sample size. In two sample problems, $N$ is usually the size of combined samples.
- When we are talking about tie
  - $g$ denotes the number of tied groups among all sample observations in the construction of test statistic
  - $t_j$ is the size of tied group $j$
  - $r_j$ is the average score associated with the observations in tied group $j$

[1]: .\OneSampleLocation\Readme.md "One Sample Location Problem"
[2]: .\OneSampleLocation\Sign_Test.md "Sign Test"
[3]: .\OneSampleLocation\Wilcoxon_Signed_Rank_Test.md "Wilcoxon Signed Rank Test"
[4]: .\TwoSampleLocation\Readme.md "Two Sample Location Problem"
[5]: .\TwoSampleLocation\Wilcoxon_Rank_Sum_Test.md "Wilcoxon Rank Sum Test"
[6]: .\TwoSampleLocation\Mann_Whitney_Test.md "Mann-Whitney Test"
[7]: .\TwoSampleLocation\Fligner_Policello_Test.md "Fligner_Policello Test"
[8]: .\TwoSampleDispersion\Readme.md "Two-Sample Dispersion Problem"
[9]: .\TwoSampleDispersion\Ansari_Bradley_Test.md "Ansari-Bradley Test"
[10]: .\TwoSampleDispersion\Siegel_Tukey_Test.md "Siegal Tukey Test" 
[11]: .\TwoSampleDispersion\Lepage_Test.md "Lepage Test" 
[12]: .\TwoSampleDispersion\Kolmogorov_Smirnov_Test.md "Kolmogorov-Smirnov Test"

