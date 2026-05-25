# NewsImages Challenge Submission

## Group Information

- Group Name: FAST-MS
- Institution: FAST National University of Computer and Emerging Sciences
- Program: Master of Science in Data Science
- Submission Date: May 2026

---

# Overview

This repository contains our submission for the MediaEval 2026 NewsImages Challenge. The task is to recommend or generate a relevant image for a given news article title.

Our submission includes both retrieval-based and generation-based approaches. Retrieval methods identify the most relevant image from the provided training collection, while the generation method creates a new image directly from the article title.

---

# Methodology

Our solution consists of two components:

1. Retrieval-Based Image Recommendation
2. Text-to-Image Generation

---

# Retrieval-Based Approaches

## 1. Official Retrieval Baseline

The organizer-provided retrieval baseline was used as a reference system.

### Components

- OpenCLIP image-text embeddings
- Cosine similarity matching

---

## 2. Hybrid Retrieval

A weighted retrieval approach combining semantic and lexical similarity measures.

### Components

- OpenCLIP embeddings
- BGE semantic embeddings
- TF-IDF similarity

### Weighted Fusion

- CLIP Similarity: 30%
- BGE Similarity: 50%
- TF-IDF Similarity: 20%

---

## 3. Basic Retrieval

A semantic retrieval system based solely on dense text embeddings.

### Components

- BAAI BGE Base EN v1.5
- Cosine similarity retrieval

---

# Generative Approach

## RealVisXL Generation

Images were generated directly from article titles using RealVisXL V5.0.

### Generation Settings

- Resolution: 512 × 512
- Inference Steps: 6
- Guidance Scale: 4.0
- CPU Offloading Enabled
- Memory-Efficient Attention Enabled

---

# Dataset Utilized

- Training Dataset: 8,500 news articles with associated images
- Test Dataset: 800 article titles requiring image recommendation or image generation

---

# Submitted Runs

| Run ID | Method |
|---------|---------|
| 1 | Official Retrieval Baseline |
| 2 | Hybrid Retrieval |
| 3 | Basic Retrieval |
| 4 | RealVisXL Generation |

---

# Key Technologies

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Diffusers
- OpenCLIP
- BGE Embeddings
- TF-IDF
- RealVisXL

---

# Notes

- Embeddings were precomputed and cached to improve retrieval efficiency.
- Experiments were conducted using Google Colab and Kaggle environments.
- RealVisXL was optimized using memory-efficient inference settings to accommodate limited computational resources.

---

# Contact

- Team: FAST-MS
- Institution: FAST National University of Computer and Emerging Sciences

---

# External Storage

The submitted run files and generated images are available at:

Google Drive: [https://drive.google.com/drive/folders/1GuLpKhCkggC8is65pjrXlatwgCXHxqDF?usp=drive_link](https://drive.google.com/drive/folders/1GuLpKhCkggC8is65pjrXlatwgCXHxqDF?usp=drive_link)]
---

# Acknowledgment

We thank the MediaEval NewsImages organizers for providing the dataset, benchmark framework, and evaluation resources.
