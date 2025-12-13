# Statistics for data analytics

Module: Applied Statistics
Author: Finian Doonan

This repository contains a Jupyter Notebook implementing four statistical exercises: extensions of the Lady Tasting Tea experiment, sampling from normal distributions, t-tests, and ANOVA.

---

## Problem 1: Extending the Lady Tasting Tea

**Objective:**  
Extend Fisher's Lady Tasting Tea experiment to 12 cups (8 tea-first, 4 milk-first) and estimate the probability that a participant correctly identifies all cups by chance.([Lady Tasting Tea](https://en.wikipedia.org/wiki/Lady_tasting_tea)).

**Simulation Steps:**
1. Represent cups as a list: 8 tea-first (`T`) and 4 milk-first (`M`).
2. Shuffle the list randomly many times.
3. Count how often the participant correctly identifies all cups by chance.
4. Estimate the probability by dividing the count by the total number of simulations.
5. Compare the probability with the original 8-cup experiment.




---

## Problem 2: Normal Distribution

**Objective:**  
Compare sample standard deviation (`ddof=1`) and population standard deviation (`ddof=0`) for small samples from the standard normal distribution. ([NumPy std documentation](https://numpy.org/doc/stable/reference/generated/numpy.std.html)).


**Steps:**
1. Generate 100,000 samples of size 10 from a standard normal distribution.
2. Compute the standard deviation for each sample using `ddof=1` and `ddof=0`.
3. Plot histograms of both sets of standard deviations on the same axes with transparency.
4. Describe differences and predict how they change as sample size increases.

---

## Problem 3: t-Tests and Type II Error

**Objective:**  
Investigate how Type II error rate changes with increasing mean difference between two samples.
 ([SciPy t-test](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_ind.html)).

**Simulation Steps:**
1. For each mean difference `d = 0, 0.1, ..., 1.0`:
   - Draw two samples of size 100: one from standard normal, one from normal with mean `d`.
   - Run an independent t-test and record if the null hypothesis is not rejected.
2. Repeat 1,000 times for each `d`.
3. Plot the proportion of times the null hypothesis is not rejected against `d`.
4. Analyze how Type II error decreases as the mean difference increases.

---

## Problem 4: ANOVA vs t-Tests

**Objective:**  
Compare ANOVA and multiple t-tests for detecting differences in means across three groups.  ([SciPy ANOVA](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.f_oneway.html)).

**Steps:**
1. Generate three independent samples of size 30 from normal distributions with means 0, 0.5, 1 and SD=1.
2. Perform a one-way ANOVA to test equality of means.
3. Perform three independent t-tests: (1 vs 2), (1 vs 3), (2 vs 3).
4. Compare results and explain why ANOVA is preferred over multiple t-tests.

---

## Notes

- All random simulations should use a fixed seed for reproducibility (e.g., `np.random.seed(42)`).
- Plots and results should include clear labels, legends, and descriptions to facilitate interpretation.
# Statistics for Data Analytics

**Module:** Applied Statistics  
**Author:** Finian Doonan

## Overview
This repository contains a Jupyter Notebook with four simulation-based exercises covering key topics in applied statistics, including randomisation tests, sampling variability, hypothesis testing, and ANOVA. All analysis is performed using Python and is fully reproducible.

---

## Exercises

### 1. Lady Tasting Tea (Extended)
- Extension of Fisher’s classic experiment to 12 cups (8 tea-first, 4 milk-first)
- Monte Carlo simulation to estimate the probability of a perfect classification by chance
- Comparison with the original 8-cup experiment

### 2. Normal Distribution
- Sampling from a standard normal distribution
- Comparison of sample (`ddof=1`) vs population (`ddof=0`) standard deviation
- Visualisation of bias and variability for small samples

### 3. t-Tests and Type II Error
- Simulation-based analysis of Type II error rates
- Effect of increasing mean difference on statistical power
- Results summarised with informative plots

### 4. ANOVA vs Multiple t-Tests
- Comparison of one-way ANOVA and pairwise t-tests across three groups
- Illustration of inflated Type I error when using multiple t-tests
- Justification for ANOVA as the preferred method

---

## Reproducibility
- Fixed random seed used throughout (e.g. `np.random.seed(42)`)
- All figures include labels, legends, and titles

---

## Requirements
- Python 3
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook

---

## Links

-  **Jupyter Notebook:** [`statistics.ipynb`](./statistics.ipynb)
- **NumPy Documentation:** [https://numpy.org/doc/](https://numpy.org/doc/)
- **SciPy Statistics:** [https://docs.scipy.org/doc/scipy/reference/stats.html](https://docs.scipy.org/doc/scipy/reference/stats.html)
-  **Matplotlib:** [https://matplotlib.org/stable/index.html](https://matplotlib.org/stable/index.html)
- **Fisher’s Lady Tasting Tea:** [https://en.wikipedia.org/wiki/Lady_tasting_tea](https://en.wikipedia.org/wiki/Lady_tasting_tea)


