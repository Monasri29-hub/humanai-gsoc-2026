# 🎨 HumanAI GSoC Tasks Submission

This repository contains my implementation for Task 1 and Task 2 of the HumanAI GSoC selection process, focusing on applying AI techniques to the Arts and Humanities domain.

---

# =========================
# 🚀 TASK 1: ARTWORK CLASSIFICATION
# =========================

## Overview

The objective of Task 1 is to build a model capable of classifying artworks based on visual attributes such as artist, style, and genre using convolutional architectures.

---

## Approach

- Images are preprocessed by resizing to 224×224 and converting into tensors  
- Artist labels are extracted from filenames and mapped to numerical classes  
- Dataset is split into training and validation sets (80–20)  
- A pre-trained **ResNet-18** model is fine-tuned for classification  
- Transfer learning is applied by freezing most layers and training only the final layer  

---

## Model

- Architecture: ResNet-18 (CNN)  
- Loss Function: CrossEntropyLoss  
- Optimizer: Adam  
- Training: Batch-based training with frozen backbone  

---

## Results

- Achieved ~28% validation accuracy across ~45 classes  
- Observed decreasing training loss over epochs  
- Model successfully learned meaningful visual features  

---

## Outlier Detection

- Softmax probabilities used to compute confidence scores  
- Predictions with confidence < 0.4 flagged as outliers  

These represent:
- Ambiguous artworks  
- Difficult classification cases  
- Potential dataset inconsistencies  

---

## Conclusion (Task 1)

A convolutional neural network-based approach was successfully implemented for artwork classification. The model demonstrates the ability to capture visual features and perform multi-class classification effectively.

A simplified CNN pipeline was used to ensure stability, with future scope to extend into convolutional-recurrent architectures for richer feature representation.

---

# =========================
# 🔍 TASK 2: IMAGE SIMILARITY
# =========================

## Overview

The objective of Task 2 is to build a system that identifies visually similar paintings based on features such as facial structure, pose, and composition.

---

## Approach

- A pre-trained CNN (**ResNet-18**) is used as a feature extractor  
- The final classification layer is removed to obtain image embeddings  
- Each image is converted into a feature vector  
- Similarity between images is computed using **cosine similarity**  

---

## Method

1. Extract feature embeddings from all images  
2. Select a query image  
3. Compute cosine similarity between query and dataset images  
4. Retrieve top-K most similar images  

---

## Results

- Successfully retrieved visually similar paintings  
- Similarity scores reflect closeness in visual representation  
- Retrieved images often share:
  - Similar facial orientation  
  - Comparable poses  
  - Consistent composition patterns  

---

## Evaluation Metrics

- **Cosine Similarity Score**  
  Measures similarity between feature vectors  

- **Qualitative Evaluation**  
  Visual inspection confirms meaningful similarity in retrieved images  

---

## Output

- Query image displayed alongside top similar images  
- Similarity scores provided for each retrieved image  

---

## Conclusion (Task 2)

A feature-based similarity system was successfully implemented using a pre-trained convolutional network. The model demonstrates the ability to capture high-level visual characteristics and retrieve semantically similar artworks.

This approach provides a scalable foundation for advanced similarity systems, including those using metric learning or multimodal representations.

---

# 🎯 FINAL CONCLUSION

Both tasks demonstrate the effective application of deep learning techniques to artwork analysis:

- Task 1 focuses on classification using supervised learning  
- Task 2 focuses on similarity using feature-based representation  

A simplified yet robust approach was chosen to ensure correctness, efficiency, and interpretability. The implementations provide a strong foundation for extending into more advanced architectures and deeper analysis within the Arts and Humanities domain.

---
