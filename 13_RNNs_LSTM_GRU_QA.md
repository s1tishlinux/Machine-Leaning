# RNNs, LSTM, GRU — Professional Q&A

---

## Q1: What is a Recurrent Neural Network (RNN)?

**A:**  
An RNN is a type of neural network designed for sequential data (text, time series, audio). It has loops so information can persist, enabling it to process inputs of variable length.

---

## Q2: What problems do vanilla RNNs have?

- Struggle to remember long-term dependencies (vanishing gradient problem).
- Training is difficult for long sequences.

---

## Q3: What are LSTM and GRU?

- **LSTM (Long Short-Term Memory):**  
  RNN variant with gates (input, forget, output) that control information flow, allowing long-term memory.
- **GRU (Gated Recurrent Unit):**  
  Similar to LSTM but simpler; fewer gates, comparable performance.

---

## Q4: Where are RNNs, LSTM, GRU used?

- Language modeling, text generation
- Speech recognition
- Time series forecasting

---

## Q5: What does an RNN/LSTM look like in code (Keras)?

```python
from tensorflow.keras.layers import SimpleRNN, LSTM, GRU

model.add(SimpleRNN(50))
model.add(LSTM(100))
model.add(GRU(64))
```

---

## Q6: Visual Memory

```
[Input₁]→[RNN]→[RNN]→…→[RNN]→[Output]
         ↑     ↑         ↑
    (remembers previous state)
```

---

# End of Q&A
