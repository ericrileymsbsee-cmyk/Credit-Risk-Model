# Credit-Risk-Model

A demonstration of an end-to-end credit default prediction workflow — from
data preparation through model comparison — built to illustrate approach and
methodology rather than to benchmark a specific result.

> **Note on data:** This notebook runs on synthetic/dummy data generated for
> demonstration. It contains no proprietary or real customer information.

## What this shows

The goal is to predict whether a borrower will default, and — just as important
in a regulated lending context — to do so with a model whose decisions can be
explained and defended. The workflow walks through the practical trade-off
every credit modeler faces: a flexible model that captures complex patterns
versus a transparent model that a risk committee or regulator can interrogate.

## Approach

- **Two modeling lenses, compared deliberately.** A gradient-boosted tree
  ensemble (XGBoost) for predictive flexibility, alongside logistic regression
  for interpretability and direct coefficient-level explanation. Comparing the
  two is the point — it frames the accuracy-vs-transparency decision explicitly
  rather than defaulting to whichever scores highest.
- **Standard credit-risk evaluation.** Discrimination assessed with ROC/AUC and
  related rank-ordering diagnostics, rather than raw accuracy, which is
  misleading on imbalanced default data.
- **Reproducible, readable workflow.** Data prep, feature handling, model
  fitting, and evaluation laid out so the reasoning is followable end to end.

## Why it's framed this way

In regulated lending, a model is only useful if it can be validated and
defended — predictive performance alone doesn't clear a model risk review. This
notebook reflects that priority: it pairs a high-flexibility model with an
explainable baseline so the explainability cost of added complexity is visible
and quantifiable.

## Stack

Python · scikit-learn · XGBoost · pandas · Jupyter

---

*Built as a portfolio demonstration of credit-risk modeling methodology.*
