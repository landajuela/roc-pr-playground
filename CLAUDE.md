# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This repository is a playground for ROC/PR curve and classifier metrics visualization. It consists of a single self-contained HTML file (`classifier_metrics.html`) with no build step or dependencies to install.

## Development

Open `classifier_metrics.html` directly in a browser — no server required. The file loads Plotly and KaTeX from CDNs.

All logic (UI, math, plotting) lives inline in `classifier_metrics.html`. The file uses:
- **Plotly** (CDN) for interactive plots
- **KaTeX** (CDN) for LaTeX math rendering
- **Google Fonts** (Fraunces, JetBrains Mono, Inter Tight) for typography

## Architecture

Everything is in one HTML file:
- CSS in `<style>` blocks handles theming via CSS custom properties (`--bg`, `--pos`, `--neg`, `--accent`, etc.)
- JavaScript handles threshold controls, metric computation (precision, recall, F1, TPR, FPR), and Plotly chart updates
- No frameworks, no bundler, no backend
