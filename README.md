# Skin Lesion Classification using Vision Transformer (ViT)

This repository contains the implementation of a Vision Transformer (ViT) model for skin lesion classification using the **HAM10000** dataset from Kaggle.

## 📂 Dataset

**Source:** [HAM10000 - Skin Cancer MNIST Dataset](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000)
Contains ~10,000 dermatoscopic images across 7 classes of skin lesions.

To use it:
1. Install the Kaggle API:
   ```bash
   pip install kaggle
   ```
2. Download the dataset:
   ```bash
   kaggle datasets download -d kmader/skin-cancer-mnist-ham10000
   ```
3. Unzip it inside a folder:
   ```
   data/HAM10000/
   ```

---

## 🧠 Model Overview

- **Architecture:** Vision Transformer (ViT)
- **Input Size:** 224×224
- **Loss:** Cross Entropy Loss
- **Optimizer:** AdamW
- **Metrics:** Accuracy, F1-score, Confusion Matrix

---

## 🚀 Run the Project

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the training file (example):
   ```bash
   python transformer_model.py
   ```

---

## 📊 Outputs

- Best model weights → `outputs/best_model.pth`
- Confusion matrix and classification report printed after training

---

## 👩‍💻 Author

**Rashmi**

Master’s in Artificial Intelligence, Long Island University – Brooklyn

---

## 🪪 License

This project is released under the Apache 2.0 License (see LICENSE file).
