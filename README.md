# ROC Curves Explained: An Interactive Visual Guide

An interactive visualization of binary classifier metrics — open `index.html` directly in any browser, no server or install required.

## What it does

Simulates a two-feature logistic classifier in the browser. Use the sliders to control the dataset and watch every chart update in lockstep:

- **Sample size** — number of points generated
- **Class centers** — separation between the positive and negative Gaussian clusters
- **Fraction positive** — class imbalance
- **Probability threshold** — slides the decision boundary and recalculates all metrics
- **FPR cap α** — upper limit of the false-positive rate for the partial-AUC region

Preset buttons jump to instructive configurations: **Random classifier** (fully overlapping classes, J ≈ 0), **Low-FA specialist** (a positive mixture with easy outliers — mediocre global AUC but excellent in the low-FPR slice), and **Resample** redraws the dataset with a new random seed to show sampling variability.

### Panels

| Section | Contents |
|---|---|
| 01 · Input space & score distribution | Scatter with decision boundary and TP/FP/FN/TN glyphs, predicted-probability histogram |
| 02 · Outcomes | Confusion matrix, TPR / FPR / Precision / F1 / Specificity / Accuracy / Error rate |
| 03 · Threshold sweep | Precision · Recall · F1 vs. threshold, ROC curve (with AUC), Precision–Recall curve (with AUPRC) |
| 04 · Youden's J | J(τ) = TPR − FPR vs. threshold, with the optimal threshold τ★ marked |
| 05 · Low false-alarm regime | Partial AUC (ROC restricted to FPR ≤ α), Success@K (top-K precision & recall) |

## Stack

- [Plotly](https://plotly.com/javascript/) — interactive charts
- [KaTeX](https://katex.org/) — LaTeX math in metric definitions
- Vanilla JS with a seeded PRNG (Mulberry32) and Box-Muller sampling — no framework, no build step
