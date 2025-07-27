# 🖋️ Signature Forgery Detection using CNN

This project aims to detect whether a handwritten signature is genuine or forged using a Convolutional Neural Network (CNN). The model was trained on the CEDAR Signature Dataset and achieves strong performance in real-world signature classification.

---

## 📌 Overview

The goal is to classify handwritten signature images into two categories:

- ✅ Genuine  
- ❌ Forged

We built a binary classification CNN that processes grayscale signature images, extracts features, and predicts the authenticity with high confidence.

---

## 🧠 Model Architecture

- Input: 128x128 grayscale images  
- Architecture:
  - Conv2D → ReLU Activation  
  - MaxPooling  
  - Dropout (0.5)  
  - Flatten → Dense → Sigmoid  
- Loss Function: Binary Crossentropy  
- Optimizer: Adam (lr = 0.0001)  
- Extras: Data Augmentation + EarlyStopping

---

## 🧾 Dataset

- Dataset: CEDAR Signature Dataset  
- Folders:
  - full_org → Genuine signatures  
  - full_forg → Forged signatures  
- Preprocessing:
  - Resize to 128×128  
  - Grayscale → Threshold → Blur  
  - Normalize pixel values to [0, 1]

---

## 📊 Results

| Metric           | Value     |
|------------------|-----------|
| Train Accuracy   | 90.86%    |
| Test Accuracy    | 87.31%    |
| Forged Recall    | 90%       |

✅ The model performed strongly, especially in detecting forged signatures with 90% recall.

---

## 🧪 Features

- Data Augmentation (rotation, shift, zoom, shear)  
- EarlyStopping to reduce overfitting  
- Real-time testing with custom images  
- Saves model for future use

