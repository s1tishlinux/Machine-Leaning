# Activation Functions — Professional Q&A

---

## Q1: What is an activation function in neural networks?

**A:**  
An activation function is a mathematical operation applied to each neuron’s output. It introduces non-linearity, allowing neural networks to model complex relationships. Without activation functions, a neural network would behave like a linear model, no matter how many layers it has.

---

## Q2: Why are activation functions important?

- Allow networks to learn nonlinear patterns.
- Enable deep networks to approximate almost any function.
- Control output range (e.g., probability between 0 and 1).

---

## Q3: What are the most common activation functions?

| Name    | Formula                    | Range         | Best For                  |
|---------|----------------------------|---------------|---------------------------|
| ReLU    | max(0, x)                  | [0, ∞)        | Hidden layers in deep nets|
| Sigmoid | 1/(1+exp(-x))              | (0, 1)        | Output for binary tasks   |
| Tanh    | (exp(x)-exp(-x))/(exp(x)+exp(-x)) | (-1, 1)   | Hidden/output (centered)  |
| Softmax | exp(xi)/sum(exp(xj))       | (0, 1), sums to 1 | Output for multi-class    |
| Leaky ReLU | x if x>0 else αx (α small)| (-∞, ∞)      | Prevents “dead” neurons   |

---

## Q4: How do you pick the right activation function?

- **Hidden layers:** ReLU is default; try Leaky ReLU if “dead neurons” occur.
- **Output (binary):** Sigmoid (produces probability).
- **Output (multi-class):** Softmax (probabilities across classes).
- **Output (regression):** None or linear.

---

## Q5: What are vanishing and exploding gradients?

- **Vanishing gradients:** In deep nets, some activations (e.g., sigmoid, tanh) squash gradients too much, so weights stop updating (network “stalls”).
- **Exploding gradients:** Gradients grow too large, causing instability.

*ReLU helps reduce vanishing gradients, which is why it’s so widely used.*

---

## Q6: What does this look like in code (TensorFlow/Keras example)?

```python
from tensorflow.keras.layers import Dense, Activation

model.add(Dense(32, activation='relu'))     # Hidden
model.add(Dense(1, activation='sigmoid'))   # Output (binary)
model.add(Dense(3, activation='softmax'))   # Output (multi-class)
```

---

## Q7: Visual Memory

```
Input → [Activation Function] → Output
    (ReLU, Sigmoid, Tanh, etc)
```

---

# End of Q&A
