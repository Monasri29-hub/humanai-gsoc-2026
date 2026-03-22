# humanai-gsoc-2026

# 🎨 HumanAI GSoC Task 1 – Artwork Classification

This repository contains my implementation for Task 1 of the HumanAI GSoC selection process. The objective of this task is to build a model capable of classifying artworks using convolutional architectures and to analyze model performance, including identifying outliers.

---

## 🚀 Overview

In this task, I developed an image classification pipeline to identify the artist of a given artwork. The implementation focuses on building a stable and efficient system using deep learning techniques, while ensuring correctness and interpretability of results.

---

## ⚙️ Approach

- Artwork images are preprocessed by resizing them to 224×224 and converting them into tensor format.
- Artist labels are extracted from image filenames and mapped to numerical classes.
- The dataset is split into training and validation sets (80–20).
- A pre-trained **ResNet-18** model is used and fine-tuned for classification.
- Transfer learning is applied by freezing most layers and training only the final classification layer.

---

## 🧠 Model

- Architecture: ResNet-18 (Convolutional Neural Network)
- Loss Function: CrossEntropyLoss
- Optimizer: Adam
- Training Strategy: Batch-based training with frozen backbone layers for efficiency

---

## 📊 Results

- Achieved approximately **28% validation accuracy** across ~45 artist classes
- Observed decreasing training loss over epochs, indicating effective learning
- Performance is reasonable given limited training time and dataset size

---

## 🔍 Outlier Detection

Outliers are identified using model confidence:

- Softmax probabilities are computed for predictions
- The maximum probability (confidence score) is extracted
- Samples with confidence below a threshold (0.4) are flagged as outliers

These outliers typically represent:
- Ambiguous artworks
- Difficult classification cases
- Potential inconsistencies in the dataset


---

## ▶️ Running the Code

1. Open the notebook in Google Colab or Jupyter
2. Mount Google Drive if required
3. Set the dataset path
4. Run all cells sequentially

---

## 🔮 Future Improvements

- Extend to multi-task classification (artist, style, genre)
- Integrate convolutional-recurrent architectures
- Train on full dataset for improved accuracy
- Use advanced evaluation metrics (F1-score, confusion matrix)
- Apply data augmentation techniques

---

## ✅ Conclusion

A convolutional neural network-based approach was successfully implemented for artwork classification. The model demonstrates the ability to learn meaningful visual features and achieve reasonable performance within constrained resources.

A simplified CNN-based pipeline was intentionally used to ensure stability and correctness. This approach provides a strong foundation that can be extended to more advanced architectures, including convolutional-recurrent models, for deeper analysis of artistic attributes.

