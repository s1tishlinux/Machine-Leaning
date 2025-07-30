# Feature Engineering — Professional Q&A

---

## Q1: What is feature engineering?

**A:**  
Feature engineering is the process of transforming raw data into meaningful features that improve the performance of machine learning models. Good features help models learn better and generalize to new data.

**Examples:**  
- Creating “age group” from exact age
- Extracting “month” from a date column
- Text vectorization (counting words, embeddings)
- Generating polynomial features

---

## Q2: What are common steps in feature engineering?

| Step              | Description                                  |
|-------------------|----------------------------------------------|
| Feature Selection | Choosing most relevant features              |
| Feature Extraction| Creating new features from raw data          |
| Feature Encoding  | Converting categorical to numerical (one-hot, label) |
| Scaling/Normalization | Bringing features to similar ranges      |
| Handling Missing Values | Imputation or removal                  |

---

## Q3: What are common encoding techniques for categorical data?

| Technique          | When to Use                  | Description                |
|--------------------|-----------------------------|----------------------------|
| Label Encoding     | Ordinal categories           | Assigns integers to labels |
| One-Hot Encoding   | Nominal, unordered categories| Binary columns per label   |
| Target Encoding    | High cardinality, supervised | Encode based on target mean|

---

## Q4: Why is scaling important?

- Many ML algorithms (e.g., kNN, SVM, neural networks) perform better when features are on a similar scale.
- Common methods: **Standardization** (mean=0, std=1), **Min-Max Scaling** (range 0–1)

---

## Q5: What are feature selection methods?

| Method                  | Description                                  |
|-------------------------|----------------------------------------------|
| Filter (e.g., variance) | Remove features with little information      |
| Wrapper (e.g., RFE)     | Use model to select best subset              |
| Embedded (e.g., Lasso)  | Feature selection within model training      |

---

## Q6: What does feature engineering look like in code (scikit-learn example)?

```python
from sklearn.preprocessing import StandardScaler, OneHotEncoder
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X_numeric)

encoder = OneHotEncoder()
X_encoded = encoder.fit_transform(X_categorical)
```

---

## Q7: Visual Memory

```
[Raw Data] → [Feature Engineering] → [Clean Features] → [ML Model]
```

---

# End of Q&A
