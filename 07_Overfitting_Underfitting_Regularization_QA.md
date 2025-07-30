# Overfitting, Underfitting & Regularization — Professional Q&A

---

## Q1: What is overfitting in machine learning?

**A:**  
Overfitting occurs when a model learns the training data *too well*, including its noise and outliers, leading to poor performance on new, unseen data. The model "memorizes" instead of "generalizing".

---

## Q2: What is underfitting?

**A:**  
Underfitting happens when a model is too simple to capture the underlying patterns in the data, resulting in poor performance on both training and test sets. The model "fails to learn".

---

## Q3: How can you detect overfitting and underfitting?

| Symptom             | Training Accuracy | Test/Val Accuracy | Meaning         |
|---------------------|------------------|-------------------|-----------------|
| Overfitting         | High             | Low               | Model memorized |
| Underfitting        | Low              | Low               | Model too simple|
| Good Generalization | High             | High              | Model learned well |

---

## Q4: What causes overfitting?

- Too complex model (too many features, deep networks)
- Too few training examples
- Training for too many epochs
- Noisy data

---

## Q5: What is regularization and why is it important?

**A:**  
Regularization adds a penalty to the loss function to discourage complex models and help prevent overfitting.

- **L1 (Lasso):** Encourages sparsity (some weights = 0)
- **L2 (Ridge):** Penalizes large weights (shrinks them)
- **Dropout:** Randomly “drops” nodes during training (neural nets)
- **Early Stopping:** Stop training when validation error stops improving

---

## Q6: What does regularization look like in code?

```python
from sklearn.linear_model import Ridge, Lasso
ridge = Ridge(alpha=1.0)
lasso = Lasso(alpha=0.1)
ridge.fit(X_train, y_train)
lasso.fit(X_train, y_train)
```

For neural networks:

```python
from tensorflow.keras.layers import Dropout
model.add(Dropout(0.5))
```

---

## Q7: Visual Memory

```
Underfitting:   [----]----]----]----] (Too simple)
Overfitting:    [--][--][--][--][--] (Too wiggly/complex)
Just Right:     [--]---[--]---[--]--- (Fits pattern)
```

---

# End of Q&A
