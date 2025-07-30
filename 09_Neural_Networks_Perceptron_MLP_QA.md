# Neural Networks (Perceptron & MLP) — Professional Q&A

---

## Q1: What is a neural network in machine learning?

**A:**  
A neural network is a computational model inspired by the human brain, made up of layers of interconnected “neurons.” It can learn complex, non-linear relationships between inputs and outputs by adjusting weights through training.

---

## Q2: What is a perceptron?

**A:**  
The perceptron is the simplest type of neural network—a single-layer linear classifier. It computes a weighted sum of inputs, adds a bias, and passes it through an activation function (often a step function).

---

## Q3: What is a Multi-Layer Perceptron (MLP)?

**A:**  
An MLP consists of an input layer, one or more hidden layers (with nonlinear activation functions like ReLU), and an output layer. It can solve complex problems that are not linearly separable.

---

## Q4: How does learning/training happen in a neural network?

- Initialize weights randomly
- Feed input forward through layers to get output
- Calculate loss (difference between prediction and true value)
- Use **backpropagation** and an optimizer (e.g., SGD, Adam) to adjust weights
- Repeat for many epochs until model performance is good

---

## Q5: What are common activation functions and why are they needed?

| Activation      | Formula           | Purpose                  |
|-----------------|-------------------|--------------------------|
| Sigmoid         | 1/(1+exp(-x))     | Squeezes to [0,1], binary|
| Tanh            | (exp(x)-exp(-x))/(exp(x)+exp(-x)) | [-1,1], zero-centered |
| ReLU            | max(0, x)         | Fast, helps with deep nets|

---

## Q6: What are typical use-cases for MLPs?

- Tabular/classical datasets
- Basic image and signal recognition
- Simple regression and classification

---

## Q7: What does an MLP look like in code?

```python
from sklearn.neural_network import MLPClassifier
mlp = MLPClassifier(hidden_layer_sizes=(100,50))
mlp.fit(X_train, y_train)
```

---

## Q8: Visual Memory

```
[Inputs] → [Hidden Layer(s)] → [Output]
     \      |   |   |   |     /
      ------|---|---|---|----
```

---

# End of Q&A
