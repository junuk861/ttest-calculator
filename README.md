# t-test Calculator

A simple browser-based statistical calculator for performing common t-tests and one-way ANOVA directly in a web browser.

This project was built as a lightweight tool for quickly comparing experimental groups without needing to open dedicated statistical software. It is especially useful for small datasets, quick exploratory analysis, teaching, and checking statistical results during routine data analysis.

The application runs entirely in the browser using HTML, CSS, and JavaScript. No installation, server, or backend is required.

---

## Features

### t-test Calculator

The main page provides a t-test calculator for comparing two groups of numerical data.

Supported test types include:

- **Unpaired Welch t-test**
  - Recommended when two independent groups may have unequal variances.
- **Unpaired equal-variance t-test**
  - Standard Student’s t-test assuming equal variance between groups.
- **Paired t-test**
  - Used when values are matched pairwise, such as before/after measurements from the same sample.

The calculator also supports different alternative hypotheses:

- **Two-tailed test**
  - Group 1 is different from Group 2.
- **One-tailed greater-than test**
  - Group 1 is greater than Group 2.
- **One-tailed less-than test**
  - Group 1 is less than Group 2.

For each analysis, the app reports:

- Mean for each group
- SEM for each group
- Sample size
- t statistic
- Degrees of freedom
- p-value
- Significance label

---

### One-way ANOVA Calculator

The project also includes a one-way ANOVA calculator for comparing multiple groups.

The ANOVA page supports up to four groups and calculates:

-
