## Background

Accurate estimation of **body-composition outcomes**—such as **appendicular lean mass (ALM)**, **bone mineral density (BMD)**, and **body fat percentage (BFP)**—is important for monitoring metabolic health, frailty/sarcopenia risk, and other clinical decisions. However, gold-standard measurements can be costly, time-intensive, or difficult to deploy at scale. This motivates learning pipelines that translate **non-invasive, accessible measurements** into reliable body-composition estimates, especially in settings where labeled outcomes are limited.

## What this repository does

This repository accompanies our paper on predicting body composition from **3D optical imaging–derived features** using both:

* **p-Laplacian–based semi-supervised regression** (graph-based), and
* Standard **supervised baselines** (XGBoost, Neural Networks, Random Forest, Polynomial Regression, SVR, and LSSVR).

Our main approach constructs a **similarity graph** over participants in feature space and applies **p-Laplacian regularization** to leverage both **labeled and unlabeled** samples. We then benchmark this method against widely used supervised algorithms under a unified evaluation workflow (cross-validation, standardized preprocessing, consistent metrics, and reproducible result generation).

## Reproducibility and extensibility

The codebase is organized to support **reproducible experiments**—from preprocessing and model training to evaluation and result export—so the main comparisons reported in the manuscript can be reproduced.

Although the paper’s results are reported on our study dataset, the pipeline is designed to be **reusable for your own data**. You can point the scripts to your own CSV (or feature matrix), specify target columns and excluded metadata columns, and run the same training/evaluation workflow to compare p-Laplacian semi-supervised learning with strong supervised baselines on your own prediction task.
