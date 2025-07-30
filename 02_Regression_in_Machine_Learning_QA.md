# Regression in Machine Learning — Professional Q&A

---

## Q1: What is regression in machine learning?

**A:**  
Regression is a supervised learning technique where the goal is to predict a **continuous numeric value** (not a class label) based on input features. The model learns to find a mathematical relationship between input variables (features) and a target variable (output).

**Examples:**  
- Predicting house prices
- Forecasting sales or stock prices
- Estimating a person's age from a photo

---

## Q2: What are the most common types of regression?

| Regression Type    | Description                                              | Example Use-Case               |
|--------------------|---------------------------------------------------------|-------------------------------|
| Linear Regression  | Fits a straight line to data (single/multiple features) | Predicting house prices       |
| Logistic Regression| Predicts probability of class (not continuous, but related) | Email spam/not spam          |
| Polynomial Regression | Fits a curved line (higher-degree polynomial)        | Modeling growth curves        |
| Ridge/Lasso/ElasticNet| Linear regression with regularization                | Handling multicollinearity    |

---

## Q3: How does linear regression work?

- **Goal:** Find the best-fit straight line \( y = wx + b \) that minimizes the difference between predicted and actual values.
- **Process:**
  1. Model assigns weights (w) to each feature.
  2. Calculates prediction as a weighted sum.
  3. Adjusts weights to minimize a loss function (Mean Squared Error, MSE).

**Mathematical Example:**
\(
	ext{Prediction:}\ \hat{y} = w_1x_1 + w_2x_2 + ... + w_nx_n + b
\)

---

## Q4: What is regularization and why is it important in regression?

**A:**  
Regularization adds a penalty to the loss function to prevent overfitting (when the model memorizes noise).  
- **Ridge Regression (L2):** Penalizes sum of squares of coefficients.
- **Lasso Regression (L1):** Penalizes sum of absolute values of coefficients.

| Regularization | Effect                 | Best For                  |
|----------------|-----------------------|---------------------------|
| Ridge (L2)     | Shrinks coefficients  | Many small/medium features|
| Lasso (L1)     | Can zero out features | Feature selection         |

---

## Q5: How do you evaluate regression models?

| Metric           | Description                       |
|------------------|----------------------------------|
| MSE (Mean Squared Error) | Average squared error    |
| RMSE (Root MSE)  | Square root of MSE               |
| MAE (Mean Absolute Error) | Average absolute error  |
| R² Score         | Proportion of variance explained  |

---

## Q6: What are some practical challenges in regression?

- **Outliers**: Can distort the fitted line.
- **Multicollinearity**: Highly correlated features can confuse the model.
- **Nonlinear Relationships**: Linear regression may not capture curves—try polynomial regression.

---

## Q7: When would you NOT use regression?

- When your output is a **category** (use classification instead).
- When you want to predict the presence/absence of something (use logistic regression for binary outcome).

---

## Q8: What does regression look like in code (scikit-learn example)?

```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

---

## Q9: Visual Memory

```
Features (size, rooms, age)
    │
    ▼
[Regression Model]
    │
    ▼
Predicted House Price (continuous value)
```

---

# End of Q&A
