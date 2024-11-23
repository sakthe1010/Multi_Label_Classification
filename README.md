# Multi_Label_Classification
DAL Data Challenge Problem
# Multi-Label Classification for ICD10 Code Prediction

This project tackles a multi-label classification problem to predict ICD10 codes from textual embeddings using advanced machine learning techniques.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Approach](#approach)
4. [Results](#results)

---

## Introduction
This project was part of a data challenge to classify medical records into multiple ICD10 codes. The dataset consisted of 200,000 samples for training, with embeddings as features and a multi-hot target label vector.

**Key Objectives:**
- Predict multiple ICD10 codes accurately for unseen records.
- Optimize for average micro-F2 evaluation metric.

---

## Dataset

**Training Data:**
- **Size:** 200,000 samples
- **Features:** 1,024 embeddings per sample
- **Labels:** Multi-hot encoded vectors (1,400 ICD10 codes)

**Evaluation Data:**
- 99,500 samples for testing.
- Average micro-F2 as the primary evaluation metric.

---

## Approach

### 1. Data Preprocessing
- Handled missing values and normalized features.
- Transformed label vectors into sparse matrices for efficiency.

### 2. Model Development
- **Logistic Regression:** Used as a baseline.
- **Neural Networks:** Developed and fine-tuned a neural network model using TensorFlow, optimizing hyperparameters to achieve the best performance.
  
### 3. Ensemble Method
- Combined predictions from all models to reduce false negatives.
- Weighted averaging based on individual model performance.

### 4. Evaluation
- Metrics: Precision, recall, F1-score, and micro-F2.
- Cross-validation to avoid overfitting.

---
## Results

- The final model is an ensemble of various simple neural network models which produced
a score of around 0.475 with the logreg model.
- The final score we got is **0.490** with a public score of 0.489 placing in the **sixth position
overall**
