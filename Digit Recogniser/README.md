# Digit Recognizer using SVM (MNIST)

This project implements a machine learning model to recognize handwritten digits using the MNIST dataset. The goal is to classify images of digits (0–9) using Support Vector Machine (SVM) and evaluate the performance through the Kaggle Digit Recognizer competition.

---

# Dataset

The dataset used in this project is the MNIST handwritten digits dataset available in the Kaggle Digit Recognizer competition.

Dataset characteristics:

- Image size: 28 × 28 pixels
- Total features: 784 pixels
- Pixel values range: 0–255
- Classes: 10 digits (0–9)

Each row in the dataset represents a flattened image of 784 pixel values.

---

# Technologies Used

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Scikit-learn  
- Kaggle Notebook  

---

# Machine Learning Approach

The model development followed these steps:

1. Loading the dataset
2. Data preprocessing and normalization
3. Splitting data into training and validation sets
4. Applying dimensionality reduction using PCA
5. Training a Support Vector Machine classifier
6. Hyperparameter tuning
7. Generating predictions for Kaggle submission

---

# Model Experiments

Three different models were trained and submitted to analyze performance improvements.

### 1 Basic SVM Model
- Support Vector Machine trained on normalized pixel features.
- No dimensionality reduction applied.
- Kaggle accuracy: **~0.973**

### 2️ PCA + SVM Model
- Applied Principal Component Analysis (PCA) to reduce 784 features to 50 components.
- Reduced noise and improved computational efficiency.
- Kaggle accuracy: **~0.978**

### 3️ PCA + Tuned SVM Model
- Applied PCA preprocessing.
- Tuned SVM hyperparameters (**C and gamma**).
- Achieved best performance.

**Final Kaggle Score:**  
**0.98235**

---

# Repository Contents

This repository contains the following files:

- `digit-recognizer.ipynb` – Kaggle notebook with full implementation
- `submission(4).csv` – Final predictions submitted to Kaggle
- `Rank of digit recogniser.png` – Kaggle leaderboard ranking screenshot
- `Submission of digit recogniser.png` – Screenshot of submission results
- `README.md` – Project documentation

---

# Kaggle Competition

Competition link:  
https://www.kaggle.com/competitions/digit-recognizer

---

# Conclusion

The experiment demonstrates that Support Vector Machines perform effectively for handwritten digit classification. Applying dimensionality reduction using PCA improves efficiency and slightly increases accuracy. Further improvement was achieved through hyperparameter tuning of the SVM model. The final model achieved a Kaggle leaderboard score of **0.98235**, showing that SVM combined with PCA is a strong approach for the MNIST digit recognition problem.

---
