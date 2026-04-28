# Lecturer Guidance

[← Back to Home](README.md) | [Programme](programme.md)

---

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

---

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

### Out of Scope

- Substantive ML teaching
- Method comparison or theory
- Advanced coding tasks

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

### Out of Scope

- Broad AI survey
- Unsupervised-learning overview
- Deep-learning survey
- Proof-heavy statistical derivations

### Learning Outcomes

Participants should be able to:

- frame an engineering prediction problem as supervised learning
- explain leakage and poor validation design
- choose suitable regression metrics
- distinguish in-domain from out-of-domain use

---

## Day 1 PM — Lab 1: Baseline CHF Regression Model

### Purpose

Build the first correct end-to-end workflow before introducing more complex models.

### In Scope

- Preprocessing
- Train / validation / test split
- Linear regression / Ridge regression
- Parity and residual plots
- Pipeline saving and reproducibility

### Outputs

- One working baseline pipeline
- At least one metric table
- Parity and residual plots
- Short note on strengths and limitations

---

## Day 2 AM — Tree Ensembles

### Purpose

Teach practical workhorse methods for structured engineering data.

### In Scope

- Decision-tree intuition
- Random Forest
- Gradient Boosting
- Why tree ensembles work well on tabular engineering data
- Practical hyperparameters and limited-budget tuning
- Regime-wise diagnostics and cautious interpretation tools

### Out of Scope

- Exhaustive hyperparameter theory
- Library benchmarking wars
- Advanced explainability methods as a major topic

---

## Day 2 PM — Lab 2: Tree Ensemble Diagnostics

### Purpose

Move from “best score wins” to engineering comparison of model behaviour.

### Outputs

- RF and GB comparison
- Regime-wise error table or plot
- One interpretability plot
- Short engineering recommendation

---

## Day 3 AM — Surrogate Modelling and Gaussian Processes

### Lecture 3.1 — Surrogate Modelling

**Purpose:** Introduce surrogate modelling as a distinct engineering task.

#### In Scope

- Emulator versus reduced model
- Simple regression surfaces, tree-based surrogates, GP surrogates, POD-style approaches
- Inputs / outputs, scaling, coverage, validation in parameter space
- Extrapolation and regime change

### Lecture 3.2 — Gaussian Process Regression

**Purpose:** Introduce GP regression as a practical surrogate model with prediction and uncertainty.

#### In Scope

- GP intuition
- GP as a distribution over functions
- Kernels as behaviour / smoothness assumptions
- Mean prediction and uncertainty
- Interpolation versus extrapolation

#### Out of Scope

- Full Bayesian derivation
- Advanced kernel design
- Large-scale sparse GP methods
- Heavy theoretical proofs

---

## Day 3 PM — Lab 3: GP Surrogate and Extrapolation Testing

### Purpose

Make GP surrogate behaviour and limitations concrete.

### Outputs

- Trained GP surrogate
- Interpolation / extrapolation comparison
- Uncertainty visualisation
- Short comparison against a tree-based method

---

## Day 4 AM — Neural Networks and Physics-based Guardrails

### Purpose

Demystify small tabular neural networks without turning the session into a deep-learning survey.

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

### Out of Scope

- PINNs as a core topic
- Operator learning
- Transformers
- Broad deep-learning survey

---

## Day 4 PM — Lab 4: Tabular Neural Network

### Purpose

Train a small MLP and evaluate it in engineering terms.

### Outputs

- Trained small MLP
- Training / validation curves
- Comparison against previous models
- Brief note on where the model should and should not be trusted

---

## Day 5 AM — VVUQ and Optimisation

### Lecture 5.1 — Introduction to VVUQ

**Purpose:** Introduce uncertainty and credibility concepts for engineering decision-making in NTH.

#### In Scope

- Why uncertainty matters in NTH decisions
- Link between model output and engineering consequence
- Aleatoric and epistemic uncertainty
- Intuitive introduction to VVUQ
- Trustworthiness beyond average accuracy

### Lecture 5.2 — UQ for Decisions and Safety-critical ML

**Purpose:** Show how uncertainty supports safer decisions and more trustworthy ML use.

#### In Scope

- Uncertainty in ML predictions
- Calibration and coverage
- Uncertainty-aware decision support
- Safe-use, caution, and do-not-use logic
- Validation and presentation of models for safety-conscious contexts
- Credibility, trustworthiness, and limits of ML tools in NTH

### Lecture 5.3 — Optimisation: Turning ML Models into Decisions

**Purpose:** Show how trained ML models can be used in simple decision-support or optimisation workflows.

#### In Scope

- Simple constrained optimisation using a surrogate or ML model
- Uncertainty-aware objective or filtering
- Feasibility and validity checks
- Difference between prediction and decision

---

## Day 5 PM — Guest Talks and Closing Discussion

### Purpose

Broaden participants’ perspective beyond the core curriculum and close the week with clear take-home lessons.

### Suggested Structure

- Short introduction
- 3–4 guest talks
- Q&A
- Programme synthesis
- Closing discussion

### Guest Talks Should

- Broaden perspective
- Connect to realistic research or engineering applications
- Avoid introducing major new required material

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
