# DeepLearning

# 🤖 Alphabet Soup Charity – Deep Learning Classification
## 📌 Overview

Alphabet Soup, a nonprofit organization, is interested in identifying applicants who are most likely to succeed if awarded funding. Using a historical dataset of over 34,000 past applicants, we develop and evaluate a binary classification model using deep learning techniques.

---

## 🧪 Objectives

- Preprocess structured data for neural network modeling
- Build a baseline neural network with Keras
- Optimize the model through tuning and architecture adjustments
- Evaluate accuracy and performance against target metrics

---

## 📊 Key Steps

### Step 1: Preprocessing
- Dropped irrelevant columns (`EIN`, `NAME`)
- Merged rare categorical values into `"Other"` buckets
- One-hot encoded categorical variables using `pd.get_dummies()`
- Scaled numeric features with `StandardScaler()`
- Split data into `X_train`, `X_test`, `y_train`, `y_test`

### Step 2: Initial Model (Baseline)
- **3 Layers**: Input + 2 Hidden + Output
- **Activations**: ReLU + Sigmoid
- Compiled with **binary_crossentropy**
- Trained with 100 epochs and checkpoint callback

### Step 3: Optimization
- Adjusted architecture:
  - Added hidden layer
  - Increased neurons in layers
  - Changed epoch count
- Model trained on new architecture and evaluated

---

## 📈 Results

### Original Model Performance:
- **Accuracy**: ~72%
- **Loss**: ~0.55
- Target (75%) not achieved.

### Optimized Model Performance:
- **Accuracy**: ~77%
- **Loss**: ~0.49
- Optimization successful! 🎯

---

## 🧠 Recommendations

- This deep learning model is a solid start, especially post-optimization.
- Further improvement can include:
  - Hyperparameter tuning via GridSearchCV (via scikit-learn wrapper)
  - Experimentation with dropout layers or regularization
  - Alternate models: Random Forests or XGBoost (for tree-based feature strength)

---

## 💾 Output Files

- `AlphabetSoupCharity.h5`: Original model
- `AlphabetSoupCharity_Optimization.h5`: Optimized model

---

## 📁 Repository Structure

```
deep-learning-challenge/
├── AlphabetSoupCharity_Custom.ipynb
├── AlphabetSoupCharity_Optimization_Custom.ipynb
├── AlphabetSoupCharity.h5
├── AlphabetSoupCharity_Optimization.h5
├── Resources/
│   └── charity_data.csv
└── README.md
```

---

## ✅ Summary

This project showcases the application of deep learning for real-world nonprofit use cases. The model successfully identifies likely successful applicants, and optimization brings it above the performance threshold.

