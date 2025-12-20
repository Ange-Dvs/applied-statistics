# applied_statistics
Repo for Applied Statistics, Semester 4 module for Data Analytics H.Dip.
The Jupyter notebook combines the theory, simulation, visualisation, and interpretation to demonstrate understanding of core statistical concepts.


Cloning repository from GitHub
Copy the following URL: https://github.com/Ange-Dvs/applied-statistics.git

Open CMDER or if using VS Code open the terminal pane

Navigate to the folder where you want to clone the repository to on your machine and type git pull git clone https://github.com/Ange-Dvs/applied-statistics.git

Set merge as the mode for the pull git config pull.rebase false

Initiate the pull of the GitHub repository git pull

If the pull has been successful, you should see folders (XXXX) and files (XXXX).

## Libraries Used

The following Python libraries are used throughout the notebook:

> math – factorials and combinatorics

> itertools – generating combinations

> random – random sampling

> numpy – numerical simulation and array operations

> pandas – tabular summaries of results

> matplotlib – plotting histograms and charts

> scipy.stats – statistical tests (t-tests, ANOVA)

All libraries are part of the standard scientific Python ecosystem.

## Repository Contents

* `problems.ipynb` 
  Main notebook containing:

  * Problem statements
  * Mathematical background
  * Python implementations
  * Visualisations
  * Interpretation and discussion


## Problem Overview

### **Problem 1 – Extending the Lady Tasting Tea Experiment**

This problem extends Ronald Fisher’s classic *Lady Tasting Tea* experiment.

**Original design:**

* 8 cups total (4 tea-first, 4 milk-first)

**Extended design:**

* 12 cups total (8 tea-first, 4 milk-first)

#### Objectives

* Compute the probability of correctly identifying all milk-first cups **by chance**
* Compare the original and extended experiments
* Discuss whether the p-value threshold (α = 0.05) should be changed

#### Key Techniques

* Combinatorics (binomial coefficients)
* Simulation using random permutations
* Probability calculations
* Visualisation of overlap counts

#### Key Result

* Original experiment:
  ( P(4\ \text{correct}) = 1/70 \approx 1.43% )

* Extended experiment:
  ( P(4\ \text{correct}) = 1/495 \approx 0.20% )

The extended design is **more stringent**, making perfect guessing substantially less likely by chance.

---

### **Problem 2 – Sampling Distribution of the Standard Deviation**

This problem explores how the definition of standard deviation affects its sampling distribution.

#### Setup

* 100,000 samples
* Sample size = 10
* Data drawn from a standard normal distribution

#### Comparisons

* **Population SD**: `ddof = 0`
* **Sample SD**: `ddof = 1`

#### Observations

* Both distributions have similar shapes
* `ddof = 0` underestimates variability for small samples
* `ddof = 1` corrects this bias

#### Extension

The simulation is repeated for increasing sample sizes (30, 100, 2500), showing:

* Reduced variability
* Convergence of the two SD definitions as sample size increases

---

### **Problem 3 – Type II Error and t-tests**

This problem investigates how the **Type II error rate** changes as the true mean difference increases.

#### Simulation Design

* Two independent samples (n = 100)
* Mean difference ( d = 0, 0.1, \dots, 1.0 )
* 1,000 repetitions per value of ( d )
* Independent two-sample t-test (α = 0.05)

#### Output

* Proportion of times the null hypothesis is **not rejected**
* Line plot of Type II error rate vs ( d )

#### Interpretation

* When ( d = 0 ), failure to reject is common
* As ( d ) increases, the Type II error rate decreases
* Larger effect sizes increase test power

---

### **Problem 4 – ANOVA vs Multiple t-tests**

This problem compares one-way ANOVA with multiple pairwise t-tests.

#### Data Generation

* Three independent samples
* Sample size = 30 per group
* Means = 0, 0.5, 1.0
* Common standard deviation = 1

#### Analyses Performed

1. One-way ANOVA
2. Three pairwise two-sample t-tests

#### Key Findings

* ANOVA tests a **single global hypothesis**
* Multiple t-tests inflate the Type I error rate
* ANOVA is the preferred approach when comparing more than two means

---

## Key Statistical Concepts Demonstrated

* Null and alternative hypotheses
* Exact probability vs simulation
* Sampling distributions
* Bias and variance
* Type I and Type II errors
* Statistical power
* Multiple comparisons problem

---

## ▶How to Run

1. Ensure Python 3.9+ is installed
2. Install required libraries (if missing):

   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook:

   ```bash
   jupyter notebook
   ```
4. Run cells sequentially from top to bottom

---

## References

* Fisher, R. A. (1935). *The Design of Experiments*
* Wikipedia – Lady Tasting Tea
* Penn State STAT 200
* Wasserstein et al. (2019) – Moving Beyond p < 0.05
* Simply Psychology – Understanding p-values

---

## Summary

This notebook demonstrates how **simulation, probability, and hypothesis testing** work together to support statistical reasoning.
Across all problems, results are interpreted in context, with careful discussion of assumptions, limitations, and best practices.



