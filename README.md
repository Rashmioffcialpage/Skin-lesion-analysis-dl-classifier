# Skin Lesion Classification using Vision Transformer (ViT)

> **Course:** AI700-001 (Fall 2025) – Machine Learning and Pattern Recognition  
> **University:** Long Island University – Brooklyn Campus  
> **Team Members:**  
> - Rashmi Thimmaraju  
> - Binh Diep  
> - Kartavya Mandora  
> - Kirtan Patel  
>  
> **Date:** November 7, 2025  
> **Instructor:** Prof. James (Course Instructor)

---

## 📄 Overview

Skin cancer is the **most common cancer in the United States**, affecting 1 in 5 Americans by age 70.  
Early diagnosis and treatment significantly improve survival rates, especially for **melanoma**, the most aggressive form.

This project implements a **Vision Transformer (ViT)** architecture to automatically detect and classify skin lesions from dermatoscopic images.  
Our goal is to support **AI-assisted clinical decision systems** that help dermatologists achieve faster and more accurate diagnoses.

---

## 💡 Application
AI-powered early detection tools can:
- Reduce clinical diagnostic time  
- Improve diagnostic accuracy for melanoma and other lesions  
- Support healthcare professionals in identifying malignancies at early stages  

---

## 📚 Literature Review

| Study | Approach | Accuracy |
|-------|-----------|-----------|
| **Aldealnabi et al. (2024)** | Vision Transformer for global attention & local context learning | 96% |
| **Bhimavarapu et al. (2022)** | Fuzzy GC-SCNN using segmentation & fuzzy logic | 99.75% |
| **Al-Waisy et al. (2025)** | Deep hybrid model (Mask-R-CNN + GrabCut + HRNet + attention) | 100% |

👉 **Observation:** Vision Transformers outperform traditional CNNs by capturing both global and local features.

---

## 🧩 Dataset – HAM10000 (Kaggle)

**Source:** [HAM10000 – Human Against Machine with 10,000 training images](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000)

- **Images:** 10,015 dermatoscopic images  
- **Classes:** 7 skin lesion types (benign and malignant)
- **Format:** JPEG + metadata CSV (dx, sex, localization, age)
- **Preprocessing:** Resized to 224×224, normalized, augmented (flips, contrast, rotations)

| Label | Meaning | Type |
|--------|----------|------|
| nv | Melanocytic nevi | Benign |
| mel | Melanoma | Malignant |
| bkl | Benign keratosis | Benign |
| bcc | Basal Cell Carcinoma | Malignant |
| akiec | Actinic Keratoses | Malignant |
| vasc | Vascular lesions | Benign |
| df | Dermatofibroma | Benign |

---

## ⚙️ Methodology

**Step-by-Step Pipeline**
1. **Dataset Collection:** Import HAM10000 dataset (images + metadata).  
2. **Preprocessing:** Resize, normalize, balance, augment images.  
3. **Feature Extraction:** Vision Transformer base (patch16-224).  
4. **Training:** Backpropagation using AdamW optimizer.  
5. **Evaluation:** Compute accuracy, F1, precision, recall, confusion matrix.  
6. **Comparison:** Evaluate ViT vs CNN vs prior literature.

---

## 🧠 Model Details

| Component | Description |
|------------|-------------|
| **Architecture** | Vision Transformer (ViT-Base-Patch16-224, pretrained on ImageNet) |
| **Loss Function** | Cross-Entropy Loss |
| **Optimizer** | AdamW (LR = 3e-5) |
| **Batch Size** | 32 |
| **Epochs** | 20 |
| **Frameworks** | PyTorch, Timm, Albumentations |

---

## 🚀 Run Instructions

1. **Install dependencies**
   ```bash
   pip install -r requirements.txt
