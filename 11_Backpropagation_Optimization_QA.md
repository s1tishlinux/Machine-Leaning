# Backpropagation & Optimization — Professional Q&A

---

## Q1: What is backpropagation?

**A:**  
Backpropagation is the algorithm used to train neural networks. It computes gradients of the loss function with respect to each weight by moving backwards through the network, enabling efficient weight updates.

---

## Q2: How does backpropagation work?

- Make a forward pass: compute outputs and loss for a batch.
- Compute the gradient (partial derivatives) of the loss with respect to each weight, starting from the output and moving backward.
- Use these gradients to adjust the weights via an optimizer.

---

## Q3: What is an optimizer? Why do we need it?

**A:**  
An optimizer is an algorithm that updates the weights of the model to minimize the loss. It uses the gradients calculated by backpropagation.

---

## Q4: What are the most common optimizers?

| Optimizer     | Key Idea                | Strengths                   |
|---------------|-------------------------|-----------------------------|
| SGD           | Fixed learning rate     | Simple, robust              |
| Momentum      | Uses previous gradient  | Faster convergence          |
| RMSprop       | Adaptive learning rate  | Good for RNNs               |
| Adam          | Combines momentum + adaptive | Most popular in deep learning|

---

## Q5: What is the learning rate?

**A:**  
The learning rate controls how big a step the optimizer takes on each update. Too high: may skip the minimum. Too low: slow convergence.

---

## Q6: What does backprop + optimization look like in code (TensorFlow/Keras)?

```python
model.compile(optimizer='adam', loss='mse')
model.fit(X_train, y_train, epochs=10)
```

---

## Q7: Visual Memory

```
[Inputs] → [Neural Net] → [Loss]
                    ↑
                [Backpropagation]
                    ↑
             [Optimizer Updates Weights]
```

---

# End of Q&A
