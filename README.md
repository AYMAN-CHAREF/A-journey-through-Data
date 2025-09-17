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
🏋️ Running the Project
Option 1: Use Pre-trained Models

Fastest way to reproduce results:

# Load pretrained models & histories
balanced_model = tf.keras.models.load_model('./models/balanced_model')
with open('./histories/balanced_history.pkl', "rb") as f:
    balanced_history = pickle.load(f)

Option 2: Train Models Yourself

Requires GPU (e.g., Google Colab, local CUDA setup).

balanced_model = lab_utils.create_model()
balanced_history = balanced_model.fit(
    train_dataset_final,
    epochs=10,
    validation_data=dev_dataset_final
)
🛠️ Tools & Libraries

TensorFlow / Keras
 – Model training & augmentation

NumPy
 – Array processing

scikit-learn
 – Metrics & evaluation

Matplotlib
 – Visualization

Google Colab
 – GPU training (optional)

📌 Notes

Pre-trained models are provided to save time (recommended).

Training from scratch requires GPU runtime (CPU is too slow).

Colab GPU availability may vary (retry if resources are busy).

✨ Acknowledgments

This project is inspired by data-centric AI principles taught in Andrew Ng’s Machine Learning Specialization (Coursera)
.
