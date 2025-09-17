# 🐶🐱🐦 A Journey Through Data: Data-Centric Machine Learning

This project explores the shift from **model-centric AI** to **data-centric AI** by showing how dataset quality, balance, and augmentation directly affect model performance.  

We build a simple **Convolutional Neural Network (CNN)** that classifies images into **dogs, cats, and birds**, while experimenting with:

- ⚖️ **Class imbalance**
- 📊 **Balanced datasets**
- 🌀 **Data augmentation**

Instead of modifying the model architecture, the focus is entirely on **how data impacts training, validation, and evaluation metrics**.

---

## 🚀 Project Overview

1. **Dataset Preparation**
   - Combines *Cats vs. Dogs* and *Caltech Birds* datasets.
   - Creates training and dev (validation) splits.
   - Simulates **imbalanced datasets** (20% dogs, 100% cats, 10% birds).

2. **Model Training**
   - Uses a fixed CNN architecture (`lab_utils.create_model()`).
   - Trains on:
     - **Imbalanced dataset** (shows misleading accuracy due to dominant classes).
     - **Balanced dataset** (better generalization).
     - **Augmented dataset** (reduces overfitting).

3. **Evaluation**
   - Tracks **accuracy, balanced accuracy, and confusion matrices**.
   - Demonstrates why accuracy alone can be misleading.
   - Highlights how **data augmentation** improves robustness.

---

## 📂 Repository Structure

