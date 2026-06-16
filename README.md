# Web-based t-test and ANOVA Calculator

This project is a simple web-based statistical calculator that allows users to run common statistical tests directly in a browser.

It includes two independent calculators:

1. **t-test Calculator**
2. **One-way ANOVA Calculator**

The goal of this project is to provide a lightweight and accessible tool for quickly analyzing small experimental datasets without installing statistical software such as Prism, R, Python, SPSS, or Excel add-ins.

The calculator runs entirely in the browser using HTML, CSS, and JavaScript. No backend server, database, login, or installation is required.

---

## Overview

This tool was designed for quick statistical analysis of numerical data from two or more experimental groups.

Users can paste raw numerical values into text boxes, choose the appropriate statistical test, calculate the result, visualize the data, and export the result as an Excel file.

The project currently supports:

- t-tests for comparing two groups
- One-way ANOVA for comparing multiple groups
- Basic visualization using scatter plots
- Mean and SEM summaries
- p-value calculation
- Significance annotation
- Excel export of the calculated results and raw data

---

## Calculators Included

### 1. t-test Calculator

The t-test calculator is available from the main page:

```text
index.html
```

It supports three types of t-tests:

- **Unpaired Welch t-test**
  - Used for comparing two independent groups when equal variance is not assumed.
- **Unpaired equal-variance t-test**
  - Used for comparing two independent groups when equal variance is assumed.
- **Paired t-test**
  - Used for matched or repeated measurements, such as before-and-after experiments.

The t-test calculator also supports different alternative hypotheses:

- **Two-tailed**
  - Group 1 is different from Group 2.
- **One-tailed: Group 1 > Group 2**
  - Tests whether Group 1 is significantly greater than Group 2.
- **One-tailed: Group 1 < Group 2**
  - Tests whether Group 1 is significantly less than Group 2.

For each t-test, the calculator reports:

- Group 1 mean
- Group 2 mean
- SEM for each group
- Sample size
- t statistic
- Degrees of freedom
- p-value
- Significance label

---

### 2. One-way ANOVA Calculator

The one-way ANOVA calculator is available from:

```text
anova.html
```

This calculator is used when comparing more than two groups.

The current ANOVA calculator supports up to four groups:

- Group 1
- Group 2
- Group 3
- Group 4, optional

The ANOVA calculator reports:

- Number of groups
- Total sample size
- F statistic
- Degrees of freedom between groups
- Degrees of freedom within groups
- p-value
- Significance label
- Mean and SEM for each group

It also performs pairwise post hoc comparisons using Welch-style pairwise t-tests with Bonferroni correction.

The post hoc table reports:

- Pairwise group comparison
- t statistic
- Degrees of freedom
- Bonferroni-adjusted p-value
- Significance label

---

## Data Input Format

Values can be entered directly into each group text box.

The calculator accepts numbers separated by:

- Commas
- Spaces
- Semicolons
- New lines

Example:

```text
4.2, 5.1, 5.5, 6.0
```

or

```text
4.2
5.1
5.5
6.0
```

Both formats are accepted.

---

## Visualization

After calculation, the app generates a scatter plot of the raw values.

The plot shows:

- Individual data points
- Group-level distribution
- Group mean markers

This allows users to quickly inspect whether the statistical result matches the visible pattern of the data.

---

## Excel Export

Both calculators include an Excel export function.

After running a calculation, users can export the result as an `.xlsx` file.

### t-test export

The t-test calculator exports:

- Summary statistics
- Raw data

The exported file name is:

```text
ttest_results.xlsx
```

### ANOVA export

The ANOVA calculator exports:

- ANOVA summary
- Group summary
- Post hoc comparison results
- Raw data

The exported file name is:

```text
anova_results.xlsx
```

---

## Technologies Used

This project uses:

- **HTML**
- **CSS**
- **JavaScript**
- **jStat**
  - Used for statistical distribution functions and p-value calculation.
- **Chart.js**
  - Used for plotting raw data and group means.
- **SheetJS / XLSX**
  - Used for exporting results to Excel files.

Because the project is built with plain HTML and JavaScript, it can be hosted easily with GitHub Pages.

---

## How to Use

### Option 1: Open locally

Download or clone the repository and open the HTML files directly in a browser.

```bash
git clone https://github.com/junuk861/ttest-calculator.git
cd ttest-calculator
```

Then open:

```text
index.html
```

or

```text
anova.html
```

in your web browser.

---

### Option 2: Host with GitHub Pages

This project can be hosted as a static website using GitHub Pages.

To enable GitHub Pages:

1. Go to the GitHub repository.
2. Open **Settings**.
3. Go to **Pages**.
4. Select the `main` branch.
5. Save the setting.
6. Open the generated GitHub Pages URL.

After GitHub Pages is enabled, the calculator can be accessed directly from the web.

---

## Project Structure

```text
ttest-calculator/
│
├── index.html      # Web-based t-test calculator
├── anova.html      # Web-based one-way ANOVA calculator
└── README.md       # Project documentation
```

---

## Intended Use

This calculator is intended for quick and simple statistical analysis of small numerical datasets.

Possible use cases include:

- Comparing experimental groups
- Checking results during data analysis
- Teaching basic statistics
- Quickly visualizing group differences
- Exporting summary results for record keeping

This tool is especially useful when a user wants to perform a quick statistical check without opening larger statistical software.

---

## Important Notes

This calculator is intended as a lightweight analysis tool. Users should still choose the statistical test carefully based on their experimental design.

For example:

- Use a paired t-test only when the two groups are truly matched.
- Use Welch’s t-test when two independent groups may have unequal variance.
- Use one-way ANOVA when comparing more than two groups.
- Consider whether correction for multiple comparisons is needed.
- For publication-quality analysis, verify the results with established statistical software when necessary.

---

## Limitations

Current limitations include:

- The ANOVA calculator currently supports up to four groups.
- The app does not currently test normality.
- The app does not currently test equality of variance.
- The app does not currently support repeated-measures ANOVA.
- The app does not currently support nonparametric tests.
- Group names are fixed as Group 1, Group 2, etc.
- The statistical calculations are performed client-side in JavaScript.

---

## Future Improvements

Possible future updates include:

- Custom group names
- More than four ANOVA groups
- Repeated-measures ANOVA
- Mann-Whitney U test
- Wilcoxon matched-pairs test
- Kruskal-Wallis test
- Multiple comparison options beyond Bonferroni correction
- Downloadable plots
- Better mobile layout
- Dark mode
- More detailed statistical explanations

---

## License

This project is currently provided as a simple open-source educational and research-support tool.

A license file can be added later depending on how the project will be shared or reused.

---

## Author

Created by **Junuk Lee**.

GitHub: [junuk861](https://github.com/junuk861)
