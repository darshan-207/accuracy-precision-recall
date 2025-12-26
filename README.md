# Accuracy vs Precision vs Recall — Why Accuracy Lies

This mini project is built to **understand model evaluation metrics**,  
not to chase the “best model”.

The goal is to clearly demonstrate **Accuracy, Precision, and Recall**
and how **changing the decision threshold changes model behavior**
— even when the model and data stay the same.

---

## 🎯 Objective

- Explain **why Accuracy alone is misleading**
- Show the **Precision–Recall trade-off**
- Prove that **metrics depend on business cost**, not algorithms

---

## 📊 Dataset

- **Bank Marketing Dataset (UCI)**
- Binary classification:
  - `y = yes` → client subscribed
  - `y = no` → client did not subscribe

Dataset link:  
https://archive.ics.uci.edu/ml/datasets/Bank+Marketing

---

## 🧠 Approach

1. Performed EDA to understand skew and outliers  
2. Handled skewed numerical features with log transforms  
3. Encoded categorical variables (One-Hot Encoding)  
4. Trained a **Logistic Regression** model (intentionally simple)  
5. Evaluated using:
   - Confusion Matrix
   - Accuracy
   - Precision
   - Recall
6. Changed **only the classification threshold** to observe metric shifts

---

## 🔍 Key Results

Same model. Same data. Different thresholds:

| Threshold | Precision | Recall |
|---------|----------|--------|
| 0.2 | 0.24 | 0.97 |
| 0.4 | 0.34 | 0.90 |
| 0.6 | 0.43 | 0.77 |
| 0.8 | 0.57 | 0.57 |

**Accuracy stayed ~82% across thresholds.**

---

## 📌 Key Takeaways

- Accuracy does not reveal **what kind of mistakes** the model makes
- Precision and Recall expose **false positives vs false negatives**
- A model does not have one performance —  
  **it has many behaviors, chosen by the threshold**
- Simple models are ideal for **learning and decision clarity**

---

## 🚀 Why Logistic Regression?

This project intentionally avoids complex models.

Logistic Regression:
- Makes metric trade-offs obvious
- Exposes imbalance effects clearly
- Forces correct thinking before optimization

Complex models (Trees, ANN) are better for performance,
but **they hide these lessons**.

---

## 📎 How to Run

```bash
pip install -r requirements.txt
