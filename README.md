# 🎗️ Breast Cancer Prediction Web App

This is a **machine learning-powered web application** that predicts whether a breast tumor is **benign** (non-cancerous) or **malignant** (cancerous) using **30 input features** from digitized images of fine needle aspirate (FNA) of breast masses.

Built using:
- 🧠 A custom **Logistic Regression** model (from scratch using NumPy)
- 🧪 **Wisconsin Breast Cancer Diagnostic Dataset**
- 🌐 **Streamlit** for UI & deployment

---

## 🔍 How It Works

1. The user inputs 30 tumor-related numerical values.
2. These values are normalized using pre-calculated dataset min/max.
3. The model uses logistic regression to predict the probability of malignancy.
4. Output is:
   - **🔴 Malignant (Cancerous)** if probability > 0.5
   - **🟢 Benign (Non-cancerous)** if probability ≤ 0.5

---

## 📊 About the Dataset

### 📁 Dataset Source:
Kaggle.com

### 📌 Dataset Overview

- **Instances**: 569 tumor samples
- **Target**: `diagnosis` —  
  - `M` = Malignant  
  - `B` = Benign

- **Features**: 30 real-valued input features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass.

---

### 🧬 Feature Breakdown

Each tumor has **10 base features**:
- `radius`, `texture`, `perimeter`, `area`, `smoothness`, `compactness`, `concavity`, `concave points`, `symmetry`, `fractal_dimension`

And for each of those 10, there are **3 variations**:
1. `_mean`: Mean value
2. `_se`: Standard error (uncertainty)
3. `_worst`: Worst (largest) value

Total = **10 features × 3 types = 30 inputs**

---

### Example:

| Feature                | Description                              |
|------------------------|------------------------------------------|
| `radius_mean`          | Average distance from center to perimeter |
| `concavity_worst`      | Maximum concave portions in worst case   |
| `area_se`              | Standard error in area measurement       |

---

## 🎯 Model Summary

- ✅ Custom logistic regression implementation (not from `sklearn`)
- ✅ Weights and bias trained using gradient descent
- ✅ Uses sigmoid activation to map inputs to probability

### Accuracy:
- **Training Accuracy**: ~98%
- **Testing Accuracy**: ~96%

---

