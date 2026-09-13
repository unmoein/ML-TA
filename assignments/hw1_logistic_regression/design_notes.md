# Design Notes — HW1: Logistic Regression

**Goal:** Give students hands-on practice with the full ML workflow on a simple binary classification task (student admission), rather than just fitting a model.

**Structure:**
- 10 guided steps, each with a markdown explanation and a code cell for students to fill in
- Bilingual instructions (English objectives + Persian task guidance) to match the course's student base

**Concepts targeted:**
- Handling missing data with KNN imputation (rather than naive drop/mean-fill)
- Feature scaling awareness (Exam1 on a 100-point scale vs Exam2 on a 20-point scale)
- Comparing evaluation strategies: simple train/test split vs. K-Fold cross-validation
- Visualizing convergence by tracking weight updates over SGD epochs
- Closing reflection questions on generalization and overfitting, to push beyond "make the code run"

**Dataset:** `student_admission.csv` — synthetic exam scores with an admitted/not-admitted label, with some values deliberately left missing to force use of the imputation step.
