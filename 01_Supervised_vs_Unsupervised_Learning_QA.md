# Supervised vs. Unsupervised Learning — Professional Q&A

---

## Q1: What is supervised learning?

**A:**  
Supervised learning is a type of machine learning where the model is trained on labeled data. This means each input example is paired with a correct output (target), and the model learns to map inputs to outputs.

**Examples:**  
- Predicting house prices (input: features of house, output: price)
- Email spam detection (input: email text, output: spam/not spam)
- Image classification (input: image, output: label such as 'cat' or 'dog')

---

## Q2: What is unsupervised learning?

**A:**  
Unsupervised learning is a type of machine learning where the model is trained on **unlabeled data**. The algorithm tries to find patterns or structure in the data without explicit output labels.

**Examples:**  
- Customer segmentation (grouping similar customers)
- Anomaly detection (finding unusual patterns)
- Dimensionality reduction (reducing data complexity while preserving information)

---

## Q3: What are the main differences between supervised and unsupervised learning?

| Feature                 | Supervised Learning       | Unsupervised Learning          |
|-------------------------|--------------------------|-------------------------------|
| Data                    | Labeled                  | Unlabeled                     |
| Main goal               | Predict outputs, mapping | Find structure or patterns    |
| Common tasks            | Classification, regression| Clustering, association, reduction |
| Evaluation              | Accuracy, RMSE, F1, etc. | No clear accuracy; use clustering score, silhouette, etc. |

---

## Q4: What are the challenges for each type?

- **Supervised:** Requires large labeled datasets (expensive/time-consuming).
- **Unsupervised:** Harder to evaluate; results may not be as interpretable.

---

## Q5: Where are these approaches used in real projects?

- **Supervised:** Fraud detection, diagnostics, object recognition, speech-to-text.
- **Unsupervised:** Market segmentation, recommender systems (cold start), exploratory data analysis, anomaly/fraud detection.

---

## Q6: Can you combine supervised and unsupervised learning?

**A:** Yes. Semi-supervised learning uses a small amount of labeled data and lots of unlabeled data (common in NLP, vision). Self-supervised learning is a new trend (especially in LLMs).

---

## Q7: Visual Memory

```
Supervised:   [Input + Target] ──► [Learn mapping] ──► [Predict output]
Unsupervised: [Input only]     ──► [Find pattern/group/structure]
```

---

# End of Q&A
