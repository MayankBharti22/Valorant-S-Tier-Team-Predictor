# Valorant-S-Tier-Team-Predictor

This project applies **machine learning** to **esports analytics** by predicting whether a professional **Valorant** team qualifies as an **S-Tier winner** based on historical tournament performance data.

The project emphasizes proper handling of **imbalanced data**, and **model interpretability**, rather than focusing solely on high accuracy.

---

## 📌 Problem Statement

The dataset does not explicitly label teams as winners or losers.  
Therefore, the objective is to:

> **Predict whether a Valorant team is an S-Tier winner using historical performance metrics.**

This is modeled as a **binary classification problem**:
- `1` → S-Tier Winner  
- `0` → Non S-Tier Team  

---

## 📂 Dataset

- **Source:** Kaggle — *Valorant Esports Top Earnings*
- **Type:** Aggregated team-level esports statistics

### Key Attributes
- Gold medals  
- Silver medals  
- Bronze medals  
- Earnings  
- S-Tier tournament participation  

---

## 🧠 Machine Learning Approach

- **Model:** Logistic Regression  
- **Final Features Used:**  
  - Gold  
  - Silver  
  - Bronze  

The target variable was engineered using **S-Tier participation**, and the dataset imbalance was handled using **class-weighted learning**.

---

## 📊 Key Observations

- Including the **Earnings** feature resulted in nearly **99% accuracy**, as earnings strongly correlate with S-Tier tournaments.
- To avoid trivial predictions and ensure meaningful learning, **Earnings was excluded** from the final model.
- The final model achieved approximately **80.5% accuracy** with improved detection of S-Tier teams.

---

## 📈 Feature Importance

Feature importance was derived from logistic regression coefficients:
- **Gold medals** showed the strongest positive influence on S-Tier classification
- **Bronze medals** had a moderate positive influence
- **Silver medals** showed a negative coefficient when controlling for Gold and Bronze

This aligns with real-world esports behavior, where championship wins matter more than consistent runner-up finishes.

---

## 🎯 Key Learnings

- Domain-based target engineering  
- Handling imbalanced classification problems  
- Avoiding data leakage  
- Prioritizing interpretability over raw accuracy  
- Applying machine learning to real-world esports data  

---

## 🛠️ Tools & Technologies

- Python  
- Pandas, NumPy  
- Matplotlib  
- Scikit-learn  

---

## 👤 Author

**Mayank Bharti**

---

## 📄 License

This project is intended for **educational and academic purposes**.
