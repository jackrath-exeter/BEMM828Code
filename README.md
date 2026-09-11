# Operational Analytics Readiness — Analysis Code

Code appendix for *Investigating Operational Analytics Readiness Among Manufacturing SMEs in Thailand: A Comparative Analysis with Selected Southeast Asian Economies* (BEMM828 MSc dissertation, University of Exeter).

## What's here

- **`D1-D6-WBES-Analysis-Appendix.ipynb`** — the complete, self-contained analysis pipeline. Loads the raw World Bank Enterprise Surveys (WBES) microdata for Thailand, Malaysia, Vietnam, and Indonesia; builds the six D1–D6 readiness dimensions; runs the significance tests (chi-square, Fisher's exact, Kruskal–Wallis, Mann–Whitney, Holm–Bonferroni); and — in its later sections — runs the additional robustness checks added after examiner review: Kish design-effect adjustment, a design-effect-re-tested significance table, pooled logistic regression with country fixed effects and cluster-robust standard errors, D2/D3 aggregation-rule triangulation, D6 effect sizes, the audit-threshold confound checks, criterion-validity regressions, and the percentile-rank redraw of Figure 4.3.
- **`results/`** — the aggregated, country-level outputs the notebook produces (composite scores, significance tests, rebuttal-analysis results). These are summary statistics only, not firm-level records, so they're safe to publish.
- **`requirements.txt`** — Python packages needed to run the notebook.

## Data access (important — raw microdata is intentionally NOT included)

This repository does **not** contain the raw WBES `.dta` microdata files, and they should not be added to it. WBES microdata is supplied under terms that permit academic use but prohibit redistribution, and the dissertation's own ethics chapter (Section 5.2) commits to exactly that: *"Raw data files were stored locally under the researcher's own credentials, were not redistributed, and are not included in Appendix B, which contains code only."*

To run the notebook yourself:

1. Register at the [World Bank Enterprise Surveys portal](https://www.enterprisesurveys.org) and download the individual country datasets used here: Thailand (2025–26), Malaysia (2024), Vietnam (2023), Indonesia (2023).
2. Update the `paths` dictionary near the top of the notebook to point at your local copies of the `.dta` files.
3. `pip install -r requirements.txt`
4. Run the notebook top to bottom.

## Citation

If you use this code, please cite the dissertation and the underlying data source:

> World Bank Group. (2023a, 2023b, 2024, 2026). *Enterprise Surveys* [Data sets]. https://www.enterprisesurveys.org
