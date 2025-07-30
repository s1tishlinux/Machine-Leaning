# Attention Mechanism & Seq2Seq — Professional Q&A

---

## Q1: What is the Seq2Seq (sequence-to-sequence) model?

**A:**  
A Seq2Seq model consists of an encoder (reads input sequence) and a decoder (generates output sequence). Originally used for translation and summarization.

---

## Q2: What is the attention mechanism?

**A:**  
Attention allows the model to “focus” on relevant parts of the input when generating each output element, rather than relying on a single fixed vector.

---

## Q3: Why is attention important?

- Improves performance on long sequences.
- Allows dynamic context: decoder can look at all encoder states and assign “importance” (weights).

---

## Q4: Where are Seq2Seq + Attention models used?

- Machine translation (e.g., English → French)
- Text summarization
- Question answering

---

## Q5: What does attention look like in code (Keras/TF Addons)?

```python
from tensorflow_addons.seq2seq import AttentionWrapper
# Wrap decoder with AttentionWrapper and use encoder outputs as memory
```

---

## Q6: Visual Memory

```
[Input Sequence] → [Encoder] → [All Hidden States]
                        ↓  ↘
                [Attention Weights]
                        ↓
                  [Decoder Output]
```

---

# End of Q&A
