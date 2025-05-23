# Intrusion Detection using AI Models On NSL-KDD Dataset


This project implements an Intrusion Detection System (IDS) using deep learning models. The models are trained and evaluated on the NSL-KDD dataset for both **binary** and **multi-class classification** tasks.

---

## ✅ What is Done

### 1. 📊 Data Preprocessing
- Loaded the NSL-KDD dataset (train and test splits).
- Dropped irrelevant columns such as `difficulty`.
- One-hot encoded categorical features: `protocol_type`, `service`, `flag`.
- Label-encoded attack types.
- Aligned train and test feature columns.

### 2. 🔄 Binary and Multi-Class Classification
- **Binary Classification**: Detects whether a sample is *normal* or *attack*.
- **Multi-Class Classification**: Classifies the specific type of attack (e.g., `neptune`, `smurf`, etc.).

### 3. ⚖️ Data Balancing with SMOTE
- Detected class imbalance using `Counter()`.
- Applied **SMOTE** to oversample minority classes in both binary and multi-class datasets.
- Dynamically adjusted `k_neighbors` to avoid runtime errors with small class sizes.

### 4. 🤖 Model Implementation
- ✅ **MLP (Multi-Layer Perceptron)**
- ✅ **LSTM (Long Short-Term Memory)**
- ✅ **Autoencoder + Classifier**
- ✅ **Voting Ensemble Classifier** (Random Forest + Gradient Boosting + Logistic Regression)

### 5. 📐 Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-Score
- Used **weighted average** for imbalanced classes.

### 6. 📊 Visualizations
- Confusion Matrix (raw and grouped into categories: Normal, DoS, Probe, R2L, U2R)
- ROC Curves for all models
- Class distribution plots before and after SMOTE
- Bar charts comparing F1-score, precision, recall, accuracy across models

---

