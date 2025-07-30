# CNNs (Convolutional Neural Networks) — Professional Q&A

---

## Q1: What is a CNN?

**A:**  
A Convolutional Neural Network (CNN) is a neural network specialized for processing grid-like data, such as images. It uses convolutional layers to extract features by sliding small filters across the input.

---

## Q2: Why are CNNs good for images?

- They automatically learn spatial features (edges, textures, shapes).
- Share weights (filters) across the image, reducing parameters.
- Preserve spatial relationships (nearby pixels).

---

## Q3: What are the main building blocks of a CNN?

| Layer          | Purpose                               |
|----------------|---------------------------------------|
| Convolution    | Extracts local patterns/features      |
| Activation     | Adds non-linearity (e.g., ReLU)       |
| Pooling        | Downsamples, makes features robust    |
| Fully Connected| Combines high-level features          |

---

## Q4: What are popular CNN architectures?

- LeNet (first classic)
- AlexNet (deep learning breakthrough)
- VGG (deeper, simple filters)
- ResNet (skip connections, very deep)

---

## Q5: What does a simple CNN look like in code (Keras)?

```python
from tensorflow.keras import layers, models
model = models.Sequential()
model.add(layers.Conv2D(32, (3,3), activation='relu', input_shape=(28,28,1)))
model.add(layers.MaxPooling2D((2,2)))
model.add(layers.Flatten())
model.add(layers.Dense(10, activation='softmax'))
```

---

## Q6: Visual Memory

```
[Image] → [Conv Layer] → [Pooling] → ... → [Flatten] → [Dense] → [Output]
```

---

# End of Q&A
