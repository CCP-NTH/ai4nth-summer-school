# Programme

[← Back to Home](README.md) | [Lecturer Guidance](lecturer_guidance.md)

---

## AI for Nuclear Thermal Hydraulics Summer School  
**13–17 July 2026 | STFC Daresbury Laboratory**

---

## Weekly Timetable

| Day | Morning Block | Afternoon Block |
|---|---|---|
| **Day 0** | Self-learning technical onboarding pack with virtual organiser support.<br><br>**Support:** Dr Wei Wang, Dr Yu Duan<br><br>Purpose: remove setup friction and align terminology, tools, and data structure. | Complete before Day 1.<br><br>Outputs: run starter notebook, produce one simple data plot, and confirm tools and data work correctly. |
| **Day 1** | **NTH problem framing, supervised ML, and workflow**<br><br>**Lecture 1.1:** Programme overview and NTH problem framing<br>*Lecturer: Prof. Michael Bluck, Imperial College London*<br><br>**Lecture 1.2:** Overview of ML methods<br>*Lecturer: Prof. Michael Bluck / Dr Yu Duan*<br><br>**Lecture 1.3:** ML workflow for TH and failure gallery<br>*Lecturer: Dr Yu Duan* | **Lab 1: Baselines, preprocessing pipelines, and first ML baseline model**<br><br>Focus: supervised tabular ML, preprocessing, evaluation, and Linear / Ridge regression baseline.<br><br>*Lead: Dr Yu Duan; Demonstrators: TAs* |
| **Day 2** | **Tree ensembles for engineering tabular data**<br><br>*Lead lecturer: Dr Junwen Yin, STFC*<br><br>**Lecture 2.1:** Random Forest — decision trees, RF intuition, engineering tabular data, key hyperparameters.<br><br>**Lecture 2.2:** Gradient Boosting — relationship to RF, progressive boosting logic, key tuning parameters.<br><br>Also includes cross-validation, regime-wise diagnostics, and cautious interpretability. | **Lab 2: Tree ensembles with regime-wise diagnostics**<br><br>Focus: use the CHF case study with Random Forest and Gradient Boosting; compare outputs, perform error slicing, and produce an engineering recommendation.<br><br>*Lead: Dr Junwen Yin; Demonstrators: TAs* |
| **Day 3** | **Surrogate modelling and Gaussian Processes**<br><br>**Lecture 3.1:** Surrogate modelling — what is a surrogate, major surrogate families, how to build one properly, and what can go wrong.<br>*Lecturer: Prof. Michael Bluck*<br><br>**Lecture 3.2:** Gaussian Process regression — GP concept, kernel functions, and sources of GP uncertainty.<br>*Lecturer: Dr Tim Rogers* | **Lab 3: GP surrogate and extrapolation stress test**<br><br>Focus: train and examine a GP on a controlled subset of the CHF dataset; compare interpolation and extrapolation behaviour; contrast GP with tree-based methods.<br><br>*Lead: Dr Tim Rogers; Demonstrators: TAs* |
| **Day 4** | **Neural networks for tabular engineering data and physics-guided guardrails**<br><br>*Lecturer: Dr Alex Skillen, University of Manchester*<br><br>**Lecture 4.1:** Neural networks — what an NN is, relation to other ML methods, basic training loop, and overfitting.<br><br>**Lecture 4.2:** Physics-guided ML — what it is and why physics guidance matters in NTH ML. | **Lab 4: Feed-forward neural network, guardrails, and edge-case testing**<br><br>Focus: train and examine a simple feed-forward NN on a controlled CHF dataset; apply constraints / guardrails and inspect edge cases.<br><br>*Lead: Dr Alex Skillen; Demonstrators: TAs* |
| **Day 5** | **Practical VVUQ and safe optimisation for decision support**<br><br>**Lecture 5.1:** Introduction to VVUQ — why UQ matters in NTH decisions; aleatoric vs epistemic uncertainty.<br>*Lecturer: Dr Saleh Rezaeiravesh, TBC*<br><br>**Lecture 5.2:** UQ for decisions and safety-critical ML practices — uncertainty in ML predictions, calibration, reliability, and validation for safety-conscious use.<br>*Lecturer: Dr Saleh Rezaeiravesh, TBC*<br><br>**Lecture 5.3:** Optimisation — turning ML models into decisions.<br>*Lecturer: TBC* | **Guest talks, synthesis, and closing discussion**<br><br>Short invited talks on advanced or emerging topics, followed by synthesis of key lessons and closing remarks.<br><br>*Guest speakers TBC* |

---

## Programme Outcomes

By the end of the week, participants should be able to:

- frame an engineering ML problem appropriately
- build and evaluate baseline supervised-learning models
- compare tree-based models for structured engineering data
- explain surrogate modelling and Gaussian Process regression
- train a small neural network for tabular data
- assess uncertainty and domain validity
- communicate model limitations and safe-use conditions
