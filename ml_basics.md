# 🚀 MLOps Interview Questions and Answers

This section provides practical and conceptual questions related to **Machine Learning Operations (MLOps)**, a critical skill for deploying and maintaining ML models in production environments.

---

## 🌐 MLOps Basics

### 1. What is MLOps?

**Answer:**
- MLOps (Machine Learning Operations) is a set of practices that combines **Machine Learning**, **DevOps**, and **Data Engineering** to **deploy, monitor, and manage ML models** in production reliably and efficiently.
- Focuses on:
  - Continuous integration & delivery (CI/CD)
  - Model versioning & reproducibility
  - Monitoring & retraining

---

### 2. What are the stages in a typical ML lifecycle?

**Answer:**
1. Data Collection
2. Data Preprocessing & Validation
3. Model Training
4. Model Evaluation
5. Model Deployment
6. Monitoring & Logging
7. Model Retraining

---

### 3. How does MLOps differ from traditional DevOps?

| Aspect             | DevOps                         | MLOps                                        |
|--------------------|-------------------------------|----------------------------------------------|
| Artifact           | Code binaries                 | Trained ML models, data pipelines            |
| Testing            | Unit/Integration tests        | Data validation, model performance tests     |
| Versioning         | Git for code                  | Git + DVC/MLflow for code, data & models     |
| Deployment         | Apps/Services                 | Models + pipelines                           |
| Monitoring         | Uptime, latency               | Drift, model accuracy, input anomalies       |

---

## ⚙️ Tools & Pipelines

### 4. What tools are used in MLOps pipelines?

**Answer:**
- **CI/CD:** GitHub Actions, GitLab CI, Jenkins
- **Experiment Tracking:** MLflow, Weights & Biases, Neptune.ai
- **Model Registry:** MLflow Registry, SageMaker Model Registry
- **Orchestration:** Kubeflow, Airflow, Prefect
- **Serving:** TensorFlow Serving, TorchServe, FastAPI, BentoML
- **Monitoring:** Prometheus, Grafana, WhyLabs, EvidentlyAI
- **Data Versioning:** DVC, LakeFS

---

### 5. What is a model registry?

**Answer:**
- A **model registry** is a centralized repository to **store, version, manage, and promote ML models** across environments (dev → staging → prod).
- Supports lineage tracking, rollback, and CI/CD integration.

---

## 🚀 Deployment & Scaling

### 6. What are the ways to deploy ML models?

**Answer:**
1. **Batch Inference:** Run predictions on a schedule or on bulk data
2. **Online Inference (REST APIs):** Real-time inference using FastAPI, Flask, etc.
3. **Edge Deployment:** Deploy models to mobile or IoT devices
4. **Serverless Deployment:** AWS Lambda, Azure Functions

---

### 7. What is model drift and how do you handle it?

**Answer:**
- **Model Drift** occurs when model performance degrades over time due to changing data patterns.
- Types:
  - **Concept Drift:** Relationship between input and output changes
  - **Data Drift:** Input data distribution changes
- **Mitigation:**
  - Continuous monitoring
  - Retraining pipelines
  - Alerting systems for drift

---

## 🧪 Monitoring & CI/CD

### 8. What is CI/CD in MLOps?

**Answer:**
- **CI (Continuous Integration):** Automate testing of data and model code
- **CD (Continuous Delivery):** Automate deployment of models to staging/production
- Includes steps like:
  - Automated model validation
  - Automated deployment to containers (Docker, K8s)
  - Rollback mechanisms

---

### 9. How do you monitor ML models in production?

**Answer:**
- Track metrics:
  - Model accuracy, precision, recall (if labels available)
  - Input data distribution (data drift)
  - Inference latency
- Tools: Prometheus, Grafana, Seldon Core, EvidentlyAI, WhyLogs

---

## 🧰 Advanced Questions

### 10. How do you implement reproducibility in ML projects?

**Answer:**
- Fix random seeds
- Use versioned data with DVC
- Store model config and hyperparameters
- Use Docker containers for environments
- Track everything in MLflow or similar tools

---

### 11. What is the role of Docker and Kubernetes in MLOps?

**Answer:**
- **Docker:** Packages model with all dependencies for consistent deployment.
- **Kubernetes:** Orchestrates containers, manages scaling, availability, and rolling updates for deployed ML services.

---

