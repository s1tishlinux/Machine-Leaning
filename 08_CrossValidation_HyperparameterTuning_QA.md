# Cross-Validation & Hyperparameter Tuning — Professional Q&A

---

## Q1: What is cross-validation in machine learning?

**A:**  
Cross-validation is a statistical method used to estimate the skill of a model on unseen data. It splits data into multiple parts (“folds”), trains on some, and validates on the rest, repeating the process to get a reliable performance estimate.

---

## Q2: Why is cross-validation important?

- Gives a **better estimate** of model performance than a single train-test split.
- Helps **avoid overfitting** to one specific validation set.
- Allows use of **all data** for both training and validation (rotating folds).

---

## Q3: What are the main types of cross-validation?

| Type                | Description                                   | When Used              |
|---------------------|-----------------------------------------------|------------------------|
| K-Fold              | Data split into K equal parts; each part used as validation once | Most common            |
| Stratified K-Fold   | K-fold but keeps label proportions balanced   | Imbalanced classes     |
| Leave-One-Out (LOO) | Each sample is its own validation set         | Small datasets         |
| Time Series Split   | Respects order in time series                 | Temporal data          |

---

## Q4: What is hyperparameter tuning?

**A:**  
Hyperparameter tuning is the process of selecting the best settings (hyperparameters) for a model (e.g., number of trees, learning rate, K in KNN) to maximize its performance.

---

## Q5: What are common hyperparameter tuning techniques?

| Technique        | Description                                     | Example                 |
|------------------|-------------------------------------------------|-------------------------|
| Grid Search      | Tries all combinations in a parameter grid      | All values of C, gamma  |
| Random Search    | Tries random combinations                       | Faster for big grids    |
| Bayesian Opt.    | Uses past results to guess better combinations  | Efficient, advanced     |

---

## Q6: What does cross-validation and tuning look like in code?

```python
from sklearn.model_selection import GridSearchCV, KFold

kf = KFold(n_splits=5)
grid = GridSearchCV(estimator=clf, param_grid=params, cv=kf)
grid.fit(X_train, y_train)
best_model = grid.best_estimator_
```

---

## Q7: Visual Memory

```
[All Data]
   │
[Split into Folds]
   │
[Train/Test in Turns]
   │
[Average Results]
   │
[Select Best Hyperparameters]
```

---

# End of Q&A
