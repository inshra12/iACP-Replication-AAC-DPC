# 🧬 iACP: Anticancer Peptide Classification using AAC + DPC Features

This project is a **replication of the iACP paper**, which classifies anticancer peptides (ACPs) using machine learning. It combines **Amino Acid Composition (AAC)** and **Dipeptide Composition (DPC)** features from protein sequences, and tests multiple ML models for classification accuracy.

---

## 📌 Objective

To classify protein sequences as **anticancer (ACP)** or **non-anticancer** based on extracted sequence features using classical machine learning models.

---

## 📂 Dataset

* **Source**: iACP dataset (CSV)
* **Size**: 349 samples
* **Classes**:

  * `1` = Anticancer Peptide
  * `0` = Non-Anticancer Peptide

---

## 🧪 Feature Extraction

### ✅ 1. Amino Acid Composition (AAC)

* Calculates frequency of each of the 20 standard amino acids in a protein.
* Output: 20 features per sequence.

### ✅ 2. Dipeptide Composition (DPC)

* Calculates frequency of each possible pair of amino acids (400 combinations).
* Output: 400 features per sequence.

### ✅ Combined Features:

* AAC (20) + DPC (400) = **Total 420 features**
* Final shape after combining with label column: **(349, 421)**

---

## 🧠 Machine Learning Models Used

The following models were trained and evaluated:

| Model                        | Accuracy    |
| ---------------------------- | ----------- |
| Logistic Regression          | 0.84        |
| Random Forest                | 0.90 ✅ Best |
| Decision Tree                | 0.83        |
| Naive Bayes                  | 0.70        |
| Support Vector Machine (SVM) | 0.89        |
| K-Nearest Neighbors (KNN)    | 0.81        |

Each model was trained using a 70/30 train-test split.

---

## 📊 Evaluation Metrics

* **Accuracy**
* **Confusion Matrix**
* **Precision, Recall, F1-score** (per class)

---

## 🔧 Tools & Libraries

* Python 🐍
* pandas, numpy
* scikit-learn (SVM, RF, DT, LR, NB, KNN)
* Jupyter Notebook / Google Colab

---

## 💡 Results & Insights

* **Random Forest** achieved the highest accuracy (90%)
* AAC and DPC features are effective in capturing sequence information
* This work lays the foundation for building **deep learning** models next (CNN, BiLSTM)

## 👩‍💻 Author

**Inshara Liaquat**
M.S. Software Engineering 
