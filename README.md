# GNU PSPP Web Edition

**GNU PSPP Web Edition** is a lightweight, fully functional, browser-based single-page application (SPA) that emulates the classic interface and statistical features of the desktop **GNU PSPP** software (a free, open-source replacement for IBM SPSS Statistics).

Built as a pure, zero-dependency client-side application, it enables statistical data analysis, data manipulation, syntax execution, and publication-ready tabular and graphical output right inside any modern web browser.

---

## 📸 Key Features & Interface Summary

- **Dual Spreadsheet Views:**
  - **Data View:** Dynamic grid editor for viewing and editing raw cases and numerical/text observation data.
  - **Variable View:** Metadata editor for specifying variable names, data types (`Numeric`, `String`), field width, decimal places, value labels, alignment, and measurement levels (`Scale`, `Ordinal`, `Nominal`).
- **Interactive Statistical Output Viewer:**
  - Standardized PSPP report tables with headers, stub labels, test statistics, degrees of freedom ($df$), and $p$-value indications.
  - Built-in HTML export and print utility for generated report tables and charts.
- **PSPP Syntax Console:**
  - Direct execution of standard PSPP syntax commands (`DESCRIPTIVES`, `FREQUENCIES`, `CROSSTABS`, `CORRELATIONS`, `REGRESSION`, `COMPUTE`, `SORT CASES`, `NEW DATASET.`).
- **Single-File Architecture:**
  - Entire application (UI layout, statistical execution engine, spreadsheet grid, modals, syntax interpreter, canvas chart rendering) runs within a single self-contained `.html` file.

---

## 📊 Supported Statistical Procedures

1. **Descriptive Statistics:**
   - **Frequencies:** Frequency counts, valid percentages, cumulative percentages, and automated canvas bar charts.
   - **Descriptives:** Sample size ($N$), Minimum, Maximum, Mean, Standard Deviation, and Variance.
   - **Crosstabs:** Two-way cross-tabulation matrix with optional Pearson Chi-Square ($\chi^2$) test of independence.
2. **Comparing Means:**
   - **One-Sample T-Test:** Single variable comparison against a custom test value.
   - **Independent-Samples T-Test:** Two-group mean comparison with pooled standard error calculations.
   - **One-Way ANOVA:** Analysis of variance across multiple independent groups ($F$-statistic).
3. **Correlations & Regression:**
   - **Pearson Bivariate Correlation:** Full correlation matrix for continuous variables.
   - **Linear Regression:** Simple linear model calculating intercept ($\alpha$), slope ($\beta$), standard errors, $t$-values, and an interactive scatter plot with fitted regression line.
4. **Non-Parametric Tests:**
   - **Chi-Square Test:** Goodness-of-fit / observed frequency breakdown.

---

## 🛠️ Data Manipulation & Transformations

- **New Dataset (`File > New Dataset`):** Completely resets current cases, variable definitions, and selection states, setting document name to `Untitled.sav`.
- **Compute Variable:** Supports dynamic arithmetic expressions and mathematical functions (e.g., `SQRT()`, `LOG()`, `age + 10`).
- **Recode Variables:** Map old values into new numeric or string values.
- **Sort Cases:** Quick sorting by any selected variable ascending or descending.
- **Filter / Select Cases:** Conditional expression filtering (e.g., `age > 30`).
- **Transpose & Aggregate:** Pivot variables into cases or summarize variables.
- **Undo / Redo Stack:** Full state management (`Ctrl+Z` / `Ctrl+Y`) up to 25 historical steps.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| `Ctrl + N` / `Cmd + N` | Create a **New Dataset** |
| `Ctrl + Z` / `Cmd + Z` | **Undo** last action |
| `Ctrl + Y` / `Cmd + Y` | **Redo** action |
| `Enter` | Save cell value in Data View |

---

## 📂 File Support & Data Import/Export

- **Import:** CSV (`.csv`) data files and JSON (`.json`) dataset schemas.
- **Export Data:** Export full datasets as CSV (`.csv`) or structured JSON (`.json`).
- **Export Output:** Export generated statistical output reports directly as standalone HTML (`.html`) documents.
- **Sample Datasets:** Built-in sample datasets (Employee Survey & Student Performance) available via `File > Sample Datasets...`.

---

## 🚀 Getting Started

1. Open `index.html` in any web browser (Chrome, Firefox, Safari, Edge).
2. Load a sample dataset via **File > Sample Datasets...** or import your own `.csv` file.
3. Switch between **Data View** and **Variable View** using the bottom tab bar.
4. Run statistical tests through the **Analyze** menu or by typing PSPP syntax commands into the **Syntax** console.
