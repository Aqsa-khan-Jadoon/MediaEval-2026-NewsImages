# NewsImages Challenge Submission

## Group Information

- **Group Name:** FAST-MS(DS)
- **Institution:** FAST National University of Computer and Emerging Sciences
- **Program:** Master of Science in Data Science
- **Submission Date:** May 17, 2026

---

# Overview

This repository contains our submission for the NewsImages Challenge (MediaEval 2026). The objective of the challenge is to recommend or generate a relevant image for a given news article title.

Our approach combines both **image retrieval** and **text-to-image generation** methodologies to maximize performance across diverse article types, including current events, historical archives, political news, health-related articles, and abstract concepts.

We developed and evaluated multiple retrieval and generation pipelines and submitted a set of complementary runs to capture both factual grounding and generative creativity.

---

# Methodology

Our solution consists of two primary components:

1. **Retrieval-Based Image Recommendation**
2. **Generative Image Synthesis**

---

# Retrieval-Based Approaches

Retrieval-based methods recommend an existing image from the provided training dataset by computing similarity between article titles and associated images.

## 1. Official Retrieval Baseline

The organizer-provided baseline approach was used as a reference point for benchmarking our improvements.

## 2. Hybrid Retrieval

A weighted combination of:

- CLIP image-text similarity
- BGE semantic embeddings
- TF-IDF lexical similarity

## 3. Entity-Enhanced Hybrid Retrieval (Primary Submission)

Our strongest retrieval system extends the hybrid model by incorporating named entity overlap extracted using spaCy.

### Components

- OpenCLIP ViT-L-14
- BAAI BGE Base EN v1.5
- TF-IDF Vectorizer
- spaCy Named Entity Recognition

### Weighted Fusion

- CLIP Similarity: 25%
- BGE Semantic Similarity: 45%
- TF-IDF Similarity: 10%
- Named Entity Overlap: 20%

## 4. MPNet Semantic Retrieval

Dense semantic retrieval using the Sentence Transformers `all-mpnet-base-v2` model.

---

# Generative Approaches

## 1. FLUX

Images generated using FLUX.1 Schnell.

## 2. RealVisXL

Images generated using RealVisXL V5.0.

### Generation Settings

- Resolution: 512 × 512
- Inference Steps: 6
- Guidance Scale: 4.0
- CPU Offloading Enabled
- Attention and VAE Slicing Enabled

---

# Dataset Utilized

- Training Dataset: 8,500 news articles with associated images
- Evaluation Dataset: ~12,000 articles and images
- Test Dataset: 800 article titles requiring image recommendation or generation

---

# Submitted Runs

| Run ID | Retrieval Method | Generation Model |
|------:|------------------|-----------------|
| 1 | Official Retrieval Baseline | None |
| 2 | Hybrid Retrieval | None |
| 3 | Entity-Enhanced Hybrid Retrieval | None |
| 4 | MPNet Semantic Retrieval | None |
| 5 | FLUX-Based Generation | FLUX |
| 6 | RealVisXL-Based Generation | RealVisXL |

---

# Key Technologies

- Python
- Jupyter Notebook
- PyTorch
- Hugging Face Transformers
- Hugging Face Diffusers
- Sentence Transformers
- OpenCLIP
- BGE Embeddings
- TF-IDF
- spaCy
- FLUX
- RealVisXL

---

# Notes

- Intermediate embeddings and score matrices were cached to reduce computation time.
- Kaggle and Google Colab were used for large-scale experimentation.
- SDXL models were optimized using CPU offloading and memory-efficient settings.

---

# Contact

- **Team:** FAST-MS(DS)
- **Institution:** FAST National University of Computer and Emerging Sciences

---

# Acknowledgment

We thank the MediaEval NewsImages organizers for providing the dataset, evaluation framework, and benchmark.
