# 🎓 Student Performance Prediction System

![Project Banner](file:///C:/Users/ASUS/.gemini/antigravity/brain/ee3053af-65ec-432d-8cbc-04bd74fc01ff/project_banner_1778948134042.png)

## 📌 Project Overview
This repository hosts a comprehensive **Student Performance Prediction System** designed to estimate final exam marks based on various academic and behavioral indicators. By leveraging multiple **Computational Intelligence (CI)** models—including Artificial Neural Networks (ANN), Deep Neural Networks (DNN), and Fuzzy Logic—this project provides a comparative analysis of different approaches to educational data mining.

---

## 👥 Research Team (Group 05)
| Name | Student ID |
| :--- | :--- |
| **SEE CHWAN KAI** | 242UT2449P |
| **TEO JING AN** | 242UT24490 |
| **KHO WEI CONG** | 242UT2449Z |
| **TEE KIAN HAO** | 242UT244B2 |

---

## 🚀 Key Features
- **Multi-Model Comparison**: Evaluates and compares ANN, DNN, and Rule-based Fuzzy Systems.
- **Robust Preprocessing**: Includes feature engineering (interaction terms, log transforms) and standardization.
- **Experimental Tracking**: Compares various architectures, activation functions, and learning rates.
- **End-to-End Pipeline**: From raw CSV data to performance evaluation metrics (RMSE, MAE, R²).

---

## 📊 Dataset Specifications
The system utilizes a dataset (`Final_Marks_Data.csv`) containing **2,000 student records**.

### Feature Set:
| Feature | Description | Range |
| :--- | :--- | :--- |
| `Attendance (%)` | Percentage of classes attended | 0 - 100 |
| `Internal Test 1` | Score from first internal assessment | 0 - 40 |
| `Internal Test 2` | Score from second internal assessment | 0 - 40 |
| `Assignment Score` | Continuous assessment score | 0 - 10 |
| `Daily Study Hours`| Average time spent studying per day | 1 - 5 |
| **Final Exam Marks**| **Target Variable** | 0 - 100 |

---

## 🧠 Computational Intelligence Models

### 1. Artificial Neural Network (ANN)
A shallow learning architecture focused on efficiency.
- **Structure**: Single hidden layer.
- **Config**: 32 to 128 hidden units, ReLU/Tanh activation.
- **Regularization**: Dropout (0.2).

### 2. Deep Neural Network (DNN)
A sophisticated multi-layered architecture for capturing complex non-linear relationships.
- **Structure**: 3 Hidden Layers (128 → 64 → 32).
- **Techniques**: Batch Normalization, L2 Regularization, and Dropout.
- **Optimizer**: Adam with tuned learning rates (0.001 - 0.002).

### 3. Fuzzy Logic System
A human-like reasoning system based on linguistic rules.
- **Antecedents**: Attendance, Internal Marks, Assignments, Study Hours.
- **Membership Functions**: Triangular (Low, Med, High).
- **Rule Base**: Expert-defined logic (e.g., *High Attendance & High Internal → High Exam Score*).

---

## 📈 Performance Benchmarks

The following table summarizes the best-performing configuration for each model type:

| Model | Architecture | RMSE | MAE | R² Score |
| :--- | :--- | :--- | :--- | :--- |
| **🏆 DNN** | **128-64-32 (ReLU, LR=0.002)** | **4.6882** | **3.7091** | **0.8245** |
| **ANN** | 64 Units (ReLU, LR=0.001) | 4.6957 | 3.7351 | 0.8239 |
| **Fuzzy System**| Rule-based Inference | 9.6785 | 7.6707 | 0.2520 |

> [!NOTE]
> The DNN slightly outperformed the ANN, while the Fuzzy System struggled due to the complexity of the regression task and limited rule coverage compared to the data-driven neural approaches.

---

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/sylvesterkho1113/Student_Performance_Prediction_System_Compare_With_Different_CI_Model.git
```

### 2. Install Dependencies
```bash
pip install numpy pandas scikit-learn tensorflow scikit-fuzzy
```

### 3. Run the Analysis
Open `main.ipynb` in Jupyter Notebook or Google Colab and run all cells to reproduce the results.

---

## 📑 License
This project is for educational purposes as part of a Computational Intelligence course.
