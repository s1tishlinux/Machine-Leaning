# Model Evaluation — Professional Q&A

---

## Q1: What is model evaluation in machine learning?

**A:**  
Model evaluation is the process of measuring how well your machine learning model performs, usually using a separate test set or through cross-validation. It helps to judge model accuracy, generalization, and compare between different models.

---

## Q2: What are common evaluation metrics?

| Task          | Main Metrics                            |
|---------------|-----------------------------------------|
| Regression    | MSE, RMSE, MAE, R²                      |
| Classification| Accuracy, Precision, Recall, F1, ROC-AUC|
| Clustering    | Silhouette Score, Inertia, DBI          |

---

## Q3: What do accuracy, precision, recall, and F1-score mean?

- **Accuracy:** Proportion of total correct predictions.
- **Precision:** Of predicted positives, how many are correct?
- **Recall (Sensitivity):** Of all actual positives, how many did we find?
- **F1 Score:** Harmonic mean of precision and recall.

| Metric      | Formula                                 | Best For               |
|-------------|-----------------------------------------|------------------------|
| Accuracy    | (TP+TN)/(TP+TN+FP+FN)                   | Balanced classes       |
| Precision   | TP/(TP+FP)                              | False positives costly |
| Recall      | TP/(TP+FN)                              | False negatives costly |
| F1 Score    | 2×(Prec×Rec)/(Prec+Rec)                 | Imbalanced classes     |

---

## Q4: What is cross-validation?

**A:**  
Cross-validation is a technique for assessing how the results of a model will generalize to an independent dataset. **K-fold cross-validation** splits the data into K parts, trains on K–1, tests on the last, and repeats—giving a robust estimate of performance.

---

## Q5: What is overfitting and underfitting?

- **Overfitting:** Model learns noise; high train accuracy, low test accuracy.
- **Underfitting:** Model too simple; low accuracy everywhere.

**Goal:** Find the balance so model generalizes well.

---

## Q6: What does evaluation look like in code (scikit-learn example)?

```python
from sklearn.metrics import accuracy_score, f1_score
y_pred = model.predict(X_test)
acc = accuracy_score(y_test, y_pred)
f1 = f1_score(y_test, y_pred)
```

---

## Q7: Visual Memory

```
[Train/Test Split] → [Fit Model] → [Evaluate on Test] → [Compare Metrics]
```

---

# End of Q&A
