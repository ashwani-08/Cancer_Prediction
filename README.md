# 🧬 Cancer Prediction using Logistic Regression

This project applies **Logistic Regression** to predict whether a cancer diagnosis is **Malignant (M)** or **Benign (B)** using real-world diagnostic data. The model is evaluated with key classification metrics such as **accuracy**, **precision**, **recall**, **F1-score**, and a **confusion matrix**.

---

## 📂 Dataset Overview

- **Source**: [Cancer Dataset](https://github.com/YBIFoundation/Dataset/raw/main/Cancer.csv)
- **Total Records**: `569`
- **Target Column**: `diagnosis`
  - `M` = Malignant (Cancer)
  - `B` = Benign (Non-cancer)
- **Features**: `30` numerical features representing:
  - Radius, Texture, Perimeter, Area
  - Smoothness, Compactness, Concavity
  - Symmetry, Fractal Dimension (mean, SE, worst)
- **Dropped Columns**:
  - `id` (non-informative)
  - `Unnamed: 32` (empty column)

---

## ⚙️ Operations Performed

- Loaded dataset using **pandas**
- Removed irrelevant columns: `id`, `Unnamed: 32`
- Separated data into **features** (`X`) and **target** (`y`)
- Encoded labels using **LabelEncoder** (`B` → `0`, `M` → `1`)
- Performed **train-test split** (70% training, 30% testing)
- Built a **Logistic Regression** model (`max_iter=5000`)
- Trained the model and made predictions on test data
- Evaluated performance using:
  - **Confusion Matrix**
  - **Classification Report** (Precision, Recall, F1-Score, Accuracy)

---

## 🔢 Confusion Matrix
[[97, 5],
[ 2, 67]]

- ✅ 97 **Benign** cases correctly predicted  
- ✅ 67 **Malignant** cases correctly predicted  
- ❌ 5 **False Positives** (Benign predicted as Malignant)  
- ❌ 2 **False Negatives** (Malignant predicted as Benign)

---

## ✅ Model Evaluation

### 📉 Classification Report

| Diagnosis | Precision | Recall | F1-Score | Support |
|-----------|-----------|--------|----------|---------|
| **Benign (B)**     | 0.98      | 0.95   | 0.97     | 102     |
| **Malignant (M)**  | 0.93      | 0.97   | 0.95     | 69      |
| **Accuracy**       |           |        | **0.96** | 171     |
| **Macro Avg**      | 0.96      | 0.96   | 0.96     | 171     |
| **Weighted Avg**   | 0.96      | 0.96   | 0.96     | 171     |

- 📌 **Overall Accuracy**: **96%**

---

## 📦 Requirements

Install necessary Python packages:

```bash
pip install pandas scikit-learn

