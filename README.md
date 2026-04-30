# roc-pr-playground

An interactive visualization of binary classifier metrics — open `classifier_metrics.html` directly in any browser, no server or install required.

## What it does

Simulates a two-feature logistic classifier in the browser. Use the sliders to control the dataset and watch every chart update in lockstep:

- **Sample size** — number of points generated
- **Class centers** — separation between the positive and negative Gaussian clusters
- **Fraction positive** — class imbalance
- **Probability threshold** — slides the decision boundary and recalculates all metrics

### Panels

| Section | Contents |
|---|---|
| Input space | Ground-truth scatter vs. predicted scatter at the chosen threshold |
| Score distribution & outcomes | Predicted-probability histogram, confusion matrix, TPR / FPR / Precision / F1 / Specificity / Accuracy |
| Threshold sweep | Precision · Recall · F1 vs. threshold, ROC curve (with AUC), Precision–Recall curve (with AUC) |

## Stack

- [Plotly](https://plotly.com/javascript/) — interactive charts
- [KaTeX](https://katex.org/) — LaTeX math in metric definitions
- Vanilla JS with a seeded PRNG (Mulberry32) and Box-Muller sampling — no framework, no build step
