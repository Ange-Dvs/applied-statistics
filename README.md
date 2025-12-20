# applied_statistics
Repo for Applied Statistics (Semester 4) module for Data Analytics H.Dip.
The Jupyter notebook combines the theory, simulation, visualisation, and interpretation to demonstrate understanding of core statistical concepts.

## Quick Start

1. Open CMDER or if using VS Code open the terminal pane

2. Clone this repo:   
  ```git clone https://github.com/Ange-Dvs/applied-statistics.git```   
  ```cd applied-statistics```

3. ```pip install -r requirements.txt```

4. Open the jupyter notebook

## How to Run

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

## Repository Contents

If the clone has been successful, you should see:

* `problems.ipynb` 
  Main notebook containing:

  * Problem statements
  * Mathematical background
  * Python implementations
  * Visualisations
  * Interpretation and discussion

* `README.md`
  *   Overview of the project structure, problem summaries, setup instructions, and usage guidance.

* `requirements.txt`
  *   Lists the Python dependencies required to run the notebook and reproduce the results.

* `.gitignore`
  *  Specifies files and folders to exclude from version control (e.g. virtual environments, cache files).


## Libraries & Modules Used

The following Python libraries and modules used throughout the notebook:

> ``math`` – factorials and combinatorics [[1](https://docs.python.org/3/library/math.html)]

> ``itertools`` – generating combinations [[2](https://docs.python.org/3/library/itertools.html)]

> ``random`` – random sampling [[3](https://docs.python.org/3/library/random.html)]

> ``numpy`` – numerical simulation and array operations [[4](https://numpy.org/doc/stable/)]

> ``pandas`` – tabular summaries of results [[5](https://pandas.pydata.org/docs/)]

> ``matplotlib`` – plotting histograms and charts [[6](https://matplotlib.org/stable/)]

> ``scipy.stats`` – statistical tests (t-tests, ANOVA) [[7](https://docs.scipy.org/doc/scipy/reference/stats.html)]

All libraries are part of the standard scientific Python ecosystem.

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
$P(\text{4 correct}) = \frac{1}{70} \approx 0.0143$

* Extended experiment:
$P(\text{4 correct}) = \frac{1}{495} \approx 0.0020$


The extended design is **more stringent**, making perfect guessing substantially less likely by chance.

<hr style="border: 1px dashed #999;">

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

<hr style="border: 1px dashed #999;">

### **Problem 3 – Type II Error and t-tests**

This problem investigates how the **Type II error rate** changes as the true mean difference increases.

#### Simulation Design

* Two independent samples ($n = 100$)
* Mean difference ($d \in \{0, 0.1, \dots, 1.0\}$)
* 1,000 repetitions per value of ($d$)
* Independent two-sample $t$-test ($α = 0.05$)

#### Output

* Proportion of times the null hypothesis is **not rejected**
* Line plot of Type II error rate vs ($d$)

#### Interpretation

* When ($d = 0$), failure to reject is common
* As ($d$) increases, the Type II error rate decreases
* Larger effect sizes increase test power

<hr style="border: 1px dashed #999;">

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

<hr style="border: 1px dashed #999;">

## Key Statistical Concepts Demonstrated

* Null and alternative hypotheses
* Exact probability vs simulation
* Sampling distributions
* Bias and variance
* Type I and Type II errors
* Statistical power
* Multiple comparisons problem

<hr style="border: 1px dashed #999;">

## AI Tools
Some aspects of this notebook were developed with the support of artificial intelligence (AI) tools, such as ChatGPT.
AI was used as a supplementary aid to support concept clarification, code structuring, and explanatory writing, while all simulations, analysis decisions, and interpretations remain the author’s own.

**The purpose of incorporating AI was to assist with:**
- clarifying statistical concepts
- checking code structure and readability
- troubleshooting code

### Example prompts

**Concept clarification**
- Explain the difference between Type I and Type II errors in simple terms.
- Why does the sample standard deviation use $𝑛−1$ instead of $𝑛$?

**Troubleshooting**
- Why is my Monte Carlo simulation result slightly different each time I rerun the notebook?
- My histogram overlays look cluttered — how can I improve readability without changing the data?

All analysis, simulations, and interpretations were carried out by the author.

## References

* Fisher, R. A. (1935). *Lady tasting tea*. Wikipedia.  
* *Null hypothesis*. Wikipedia.  
* Kenton, W. (n.d.). *P-value*. Investopedia.  
* Wasserstein, R. L., Schirm, A. L., & Lazar, N. A. (2020).  
* Wasserstein, R. L., Schirm, A. L., & Lazar, N. A. (2019).  
* Wasserstein, R. L., & Lazar, N. A. (2018).  
* Benjamin, D. J., et al. (2018).  
* *Statistical significance*. Wikipedia.  
* Frost, J. (n.d.).  
* McLeod, S. (n.d.).  
* Penn State Eberly College of Science. (n.d.).  
* DataCamp. (n.d.).  
* *Statistical power*. Wikiversity.  
* *Power (statistics)*. Wikipedia.  
* *Multiple comparisons problem*. Wikipedia.  
* Penn State Eberly College of Science. (n.d.).  
* *Bonferroni correction*. Wikipedia.  

Full references are provided inside the Jupyter notebook.


***
# END
