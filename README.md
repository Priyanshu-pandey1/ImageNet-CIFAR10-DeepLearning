# CIFAR-10 Image Classification using CNN (PyTorch)

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

This repository contains a Custom Convolutional Neural Network (CNN) designed to classify images from the **CIFAR-10** dataset into 10 distinct categories. The model is implemented using **PyTorch** and demonstrates high-performance feature extraction through a modular architecture.

## 🚀 Project Overview
The goal is to correctly identify objects (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck) in 32x32 color images. By leveraging multiple convolutional layers, the model learns to identify spatial patterns and local features effectively.

## 🏗️ Model Architecture
The network consists of two main components:

### 1. Feature Extraction (Convolutional Base)
* **Layer 1:** Conv2d (3 to 32 filters, 3x3 kernel, padding=1) + ReLU + MaxPool (2x2).
* **Layer 2:** Conv2d (32 to 64 filters, 3x3 kernel, padding=1) + ReLU + MaxPool (2x2).
* **Layer 3:** Conv2d (64 to 128 filters, 3x3 kernel, padding=1) + ReLU + MaxPool (2x2).
* **Flattening:** Reshaping the output into a 1D vector ($4 \times 4 \times 128$) for the classifier.

### 2. Classification (Fully Connected Head)
* **Linear Layer 1:** 2048 input features to 256 hidden units + ReLU activation.
* **Linear Layer 2 (Output):** 256 units to 10 classes.

## 📈 Training Performance
The model was trained for **10 epochs** using standard cross-entropy loss and backpropagation.

| Epoch | Training Loss |
| :--- | :--- |
| 1 | 0.4209 |
| 5 | 0.1578 |
| 10 | **0.0804** |

> **Insight:** The loss showed a consistent downward trend, indicating efficient learning and model convergence.

## 📊 Evaluation Results
* **Final Test Accuracy:** **74.31%**
* **Evaluation Protocol:** Utilized `model.eval()` and `torch.no_grad()` to ensure proper testing behavior and memory efficiency.

## 🛠️ Tech Stack
* **Language:** Python
* **Deep Learning Framework:** PyTorch (`torch`, `torch.nn`)
* **Development Environment:** Jupyter Notebook
* **Data Handling:** `torchvision` (Transforms, DataLoader)

---
Developed by **Priyanshu Pandey**
