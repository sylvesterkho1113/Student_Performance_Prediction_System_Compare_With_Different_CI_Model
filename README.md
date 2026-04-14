# 🎓 Student Performance Prediction System

## 📌 Overview
This project aims to predict students' final exam performance using multiple computational intelligence models. The system applies machine learning and fuzzy logic techniques to analyze academic-related factors and estimate final exam marks.

---

## 👥 Group Members
- SEE CHWAN KAI (242UT2449P)
- TEO JING AN (242UT24490)
- KHO WEI CONG (242UT2449Z)
- TEE KIAN HAO (242UT244B2)

---

## 🧠 Models Used
1. **Artificial Neural Network (ANN)**
   - Single hidden layer
   - Configurable hidden units, activation, dropout

2. **Deep Neural Network (DNN)**
   - Multiple hidden layers
   - Batch normalization and dropout applied
   - L2 regularization included

3. **Fuzzy Logic System**
   - Rule-based inference system
   - Uses membership functions and linguistic rules

---

## 📊 Evaluation Metrics
The models are evaluated using regression metrics:
- **RMSE (Root Mean Squared Error)**
- **MAE (Mean Absolute Error)**
- **R² Score (Coefficient of Determination)**

---

## 📁 Dataset
- File: `Final_Marks_Data.csv`
- Total records: 2000
- Features:
  - Attendance (%)
  - Internal Test 1 (out of 40)
  - Internal Test 2 (out of 40)
  - Assignment Score (out of 10)
  - Daily Study Hours
  - Final Exam Marks (target)

---

## ⚙️ Data Preprocessing
- Removed missing values (none found)
- Feature engineering:
  - `internal_avg`
  - `internal_x_attendance`
  - `study_x_internal`
  - `log_study`
  - `sqrt_attendance`
- Standardization using `StandardScaler`
- Train-test split:
  - 80% training
  - 20% testing
- Validation split from training:
  - 80% train
  - 20% validation

---

## 🧪 Experiments
Multiple hyperparameter configurations were tested for ANN and DNN:
- Activation functions: `relu`, `tanh`
- Learning rates: `0.001`, `0.002`
- Dropout rates: `0.2 – 0.35`
- Hidden units and layer depth variations

---

## 📈 Results Summary

### 🟢 Best Model
**DNN (units = 128, 64, 32)**
- RMSE: **4.6882**
- MAE: **3.7091**
- R²: **0.8245**

### 🟡 ANN Performance
- Comparable performance to DNN
- Best RMSE around **4.69**

### 🔴 Fuzzy System Performance
- RMSE: **9.6785**
- MAE: **7.6707**
- R²: **0.2520**
- Lower accuracy due to limited rule coverage

---

## 🧩 Fuzzy Logic Design
Inputs:
- Attendance
- Internal marks (average)
- Assignment score
- Study hours

Output:
- Final exam marks

Rules example:
- High internal & high attendance → High exam score
- Low internal → Low exam score
- High study & medium assignment → Medium exam score

---

## 🚀 How to Run

### 1. Install dependencies
```bash
pip install numpy pandas scikit-learn tensorflow scikit-fuzzy
