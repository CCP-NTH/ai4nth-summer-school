---
layout: default
title: Lecturer Guidance
---

<main class="page">

# Lecturer Guidance

## One-page Summary for Invited Lecturers

These briefs are intended to help invited lecturers prepare sessions at a consistent level and in a consistent style across the week.

The audience is technically strong, numerate, and able to code, but new to modern machine learning. Lectures should therefore be intuitive first, practically grounded, explicit about limitations, and closely linked to engineering use in nuclear thermal hydraulics.

---

## General Guidance

| Item | Guidance |
|---|---|
| **Audience** | Researchers and engineers in nuclear thermal hydraulics with strong technical backgrounds but limited prior ML experience. |
| **Teaching level** | Conceptual and formula-aware, but not proof-heavy. Assume participants can run and edit Jupyter notebooks, but do not assume ML jargon or advanced statistics. |
| **Morning structure** | Two 50-minute lecture blocks plus a worked example / pre-lab ramp. |
| **Afternoon structure** | Guided lab, checkpoint, partially independent work, extension task, consolidation, and wrap-up. |
| **Lecture block** | Normally around 50 minutes. Where relevant, lecturers may also contribute to the worked example / pre-lab ramp. |
| **Lab block** | Full afternoon practical session. Labs should be scaffolded, stable, and runnable on standard laptops without heavy compute. |
| **Common expectation** | Explain why the method matters, how it works, what can go wrong, and how it should be used responsibly. |
| **Avoid** | Overly theoretical derivations, excessive scope drift, unstable code, large compute requirements, and unnecessary new frameworks. |

---

## Programme Context

The summer school focuses on:

- supervised ML for structured engineering data
- surrogate modelling for expensive simulations
- uncertainty-aware decision support

The main running example is:

> **Critical Heat Flux (CHF) prediction / structured thermal-hydraulics data**

The school is **not** intended to be a broad AI survey.

---

# Session Briefs

## Day 0 — Self-learning Technical Onboarding

**Format:** Self-learning preparation pack before Day 1, with virtual organiser support.  
**Expected time:** 60–90 minutes.

### Purpose

Ensure every participant can run the computing environment, open the notebooks, load the dataset, and understand terminology used throughout the week.

### In Scope

- Environment setup and package checks
- Notebook structure and file organisation
- Dataset access and split files
- Training domain, prediction domain, unsafe / out-of-domain region

### Outputs

- Starter notebook runs successfully
- One simple data plot
- Confirmation that tools, packages, and data are working

---

## Day 1 AM — Framing Engineering ML Problems

### Purpose

Establish what kind of ML the school covers, where it fits in NTH, and what correct workflow discipline looks like.

### In Scope

- Where supervised ML fits in NTH
- Mapping engineering tasks to supervised learning
- Target and feature definition
- Train / validation / test logic
- Leakage, preprocessing, scaling, and metric choice
- Domain-aware validation and common workflow failures

### Learning Outcomes

Participants should be able to frame an engineering prediction problem as supervised learning, explain leakage, choose suitable regression metrics, and distinguish in-domain from out-of-domain use.

---

## Day 1 PM — Lab 1: Baseline CHF Regression Model

### Purpose

Build the first correct end-to-end workflow before introducing more complex models.

### Outputs

- One working baseline pipeline
- At least one metric table
- Parity and residual plots
- Short note on strengths and limitations

---

## Day 2 — Tree Ensembles

### In Scope

- Decision-tree intuition
- Random Forest
- Gradient Boosting
- Practical hyperparameters and limited-budget tuning
- Regime-wise diagnostics and cautious interpretation tools

### Outputs

- RF and GB comparison
- Regime-wise error table or plot
- One interpretability plot
- Short engineering recommendation

---

## Day 3 — Surrogate Modelling and Gaussian Processes

### In Scope

- Emulator versus reduced model
- Simple regression surfaces, tree-based surrogates, GP surrogates, POD-style approaches
- Inputs / outputs, scaling, coverage, validation in parameter space
- GP intuition, kernels, mean prediction, and uncertainty
- Interpolation versus extrapolation

### Outputs

- Trained GP surrogate
- Interpolation / extrapolation comparison
- Uncertainty visualisation
- Short comparison against a tree-based method

---

## Day 4 — Neural Networks and Physics-based Guardrails

### In Scope

- Small feed-forward neural networks for tabular data
- Architecture, activations, loss, optimisation, and normalisation
- Overfitting and regularisation
- Learning curves
- Simple physics-based guardrails:
  - output bounds
  - plausibility checks
  - monotonicity or sensitivity checks
  - inference-time rules

### Outputs

- Trained small MLP
- Training / validation curves
- Comparison against previous models
- Brief note on where the model should and should not be trusted

---

## Day 5 — VVUQ, Decision Support, and Optimisation

### In Scope

- Why uncertainty matters in NTH decisions
- Aleatoric and epistemic uncertainty
- Calibration and coverage
- Safe-use, caution, and do-not-use logic
- Simple constrained optimisation using a surrogate or ML model
- Uncertainty-aware objective or filtering
- Feasibility and validity checks

### Learning Outcomes

Participants should understand how uncertainty can inform decisions, recognise the risks of optimisation without validity checks, and communicate model limitations responsibly.

---

# Common Guidance for All Lecturers

## Every Lecture Should Explain

- Why the method matters in engineering / NTH
- How it works conceptually
- What it looks like in practice
- What can go wrong
- How it should be used responsibly

## Every Lab Should Include

- Starter notebook
- Clear checkpoints
- Expected outputs
- At least one diagnostic or failure-mode discussion
- Short end-of-lab summary prompt

## Preferred Technical Style

- Lightweight Python stack
- Stable notebooks
- No heavy compute or GPU dependence unless necessary
- Practical workflows that run on standard laptops

</main>
