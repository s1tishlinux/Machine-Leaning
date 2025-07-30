# Transformers — Professional Q&A

---

## Q1: What is a Transformer model?

**A:**  
A Transformer is a deep learning model based entirely on attention mechanisms, without recurrence or convolutions. It can handle sequences in parallel and capture long-range dependencies.

---

## Q2: What are the main parts of a Transformer?

| Part     | Role                                              |
|----------|---------------------------------------------------|
| Encoder  | Reads input sequence and encodes representations  |
| Decoder  | Generates output sequence from encoded info       |
| Self-Attention | Allows each position to attend to all others|

---

## Q3: What is self-attention and why is it important?

- **Self-attention** lets each element in the sequence consider the whole sequence, enabling the model to understand context and relationships.
- Key for tasks like translation, summarization, code, and reasoning.

---

## Q4: Why are Transformers faster than RNNs?

- Process all tokens in parallel (no sequential dependency).
- Better for large datasets, long context.

---

## Q5: What are some famous Transformer models?

- BERT (encoder-only, understanding)
- GPT (decoder-only, generation)
- T5, BART (encoder-decoder, flexible tasks)
- Llama, Gemini (large LLMs)

---

## Q6: What does a Transformer look like in code (PyTorch, simplified)?

```python
from transformers import AutoModel
model = AutoModel.from_pretrained('bert-base-uncased')
```

---

## Q7: Visual Memory

```
[Input] → [Multi-Head Attention + FFN] × N → [Output]
         ↖------ Residual/Norm ------↗
```

---

# End of Q&A
