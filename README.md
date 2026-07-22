# 🥈 MediaEval 2026 NewsImages Challenge – 2nd Place Solution

[![MediaEval 2026](https://img.shields.io/badge/MediaEval-2026-blue)]()
[![Ranking](https://img.shields.io/badge/Rank-2nd%20Place-gold)]()
[![Paper](https://img.shields.io/badge/Paper-Published-success)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

Official implementation of our **2nd Place** solution for the **MediaEval 2026 NewsImages Challenge**.

Our work proposes a hybrid image recommendation framework that combines **retrieval-based methods**, **semantic search**, and **state of the art image generation** to recommend or generate visually relevant images for news article titles.

---

# 🏆 Achievements

- 🥈 **Secured 2nd Place** in the MediaEval 2026 NewsImages Challenge.
- 📄 **Research paper officially published** in the MediaEval 2026 Working Notes Proceedings.
- 🔍 Proposed a hybrid retrieval framework combining CLIP, BGE embeddings, and TF-IDF.
- 🎨 Explored both retrieval and generative approaches using **RealVisXL**.

---

# 📄 Publication

**Title**

> **Hybrid Retrieval and Generative Image Recommendation for News Articles: The FAST-MS(DS) Approach at MediaEval 2026**

**Authors**

- Aqsa Khan Jadoon
- Muhammad Rafi

📄 Paper

https://2026.multimediaeval.com/paper22.pdf

---

# 🏅 Official Competition Results

Our submission achieved **2nd Place** in the MediaEval 2026 NewsImages Challenge.

| Competition | Ranking |
|-------------|---------|
| MediaEval 2026 NewsImages Challenge | 🥈 2nd Place |

Official leaderboard:

https://github.com/Informfully/Challenges/blob/692eb1e46fc330f64a9ff29eea0fbdaff7e80c68/newsimages26/images/survey_results/_survey_results_26_ALL_TEAMS.xlsx

---

# 👥 Group Information

| Item | Details |
|------|---------|
| Team | FAST-MS |
| Institution | FAST National University of Computer and Emerging Sciences |
| Program | Master of Science in Data Science |
| Submission | May 2026 |

---

# 📖 Overview

The **MediaEval 2026 NewsImages Challenge** focuses on recommending or generating an image that best represents a news article title.

Our submission explores both **retrieval-based** and **generation-based** pipelines.

- **Retrieval methods** identify the most relevant image from the provided news image collection.
- **Generation methods** synthesize a new image directly from the article title using diffusion models.

---

# ⚙️ Methodology

Our framework consists of two major components.

## 1. Retrieval-Based Image Recommendation

Three retrieval strategies were evaluated.

### Official Retrieval Baseline

- OpenCLIP image-text embeddings
- Cosine similarity

---

### Hybrid Retrieval

Our best-performing retrieval approach combines multiple similarity measures through weighted fusion.

**Features**

- OpenCLIP embeddings
- BGE semantic embeddings
- TF-IDF similarity

**Weighted Fusion**

| Component | Weight |
|-----------|-------:|
| OpenCLIP | 30% |
| BGE Embeddings | 50% |
| TF-IDF | 20% |

---

### Basic Retrieval

A semantic retrieval system using dense embeddings.

- BAAI BGE Base EN v1.5
- Cosine similarity

---

## 2. Text-to-Image Generation

### RealVisXL V5.0

News article titles were directly converted into images using RealVisXL.

**Generation Settings**

| Parameter | Value |
|-----------|-------|
| Resolution | 512 × 512 |
| Inference Steps | 6 |
| Guidance Scale | 4.0 |
| CPU Offloading | Enabled |
| Memory Efficient Attention | Enabled |

---

# 📂 Dataset

| Dataset | Size |
|----------|-----:|
| Training Articles | 8,500 |
| Test Titles | 800 |

---

# 🚀 Submitted Runs

| Run | Method |
|------|--------|
| Run 1 | Official Retrieval Baseline |
| Run 2 | Hybrid Retrieval |
| Run 3 | Basic Retrieval |
| Run 4 | RealVisXL Generation |

---

# 🛠 Technologies

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Diffusers
- OpenCLIP
- BGE Embeddings
- TF-IDF
- RealVisXL
- Google Colab
- Kaggle

---

# 💾 External Resources

The submitted runs and generated images are available on Google Drive.

https://drive.google.com/drive/folders/1GuLpKhCkggC8is65pjrXlatwgCXHxqDF?usp=drive_link

---

# 📌 Notes

- Embeddings were precomputed and cached for faster retrieval.
- Experiments were conducted using Google Colab and Kaggle.
- Memory-efficient inference was employed to enable image generation on limited GPU resources.

---

# 📚 Citation

If you use this repository in your research, please cite our paper.

```bibtex
@inproceedings{jadoon2026mediaeval,
  title={Hybrid Retrieval and Generative Image Recommendation for News Articles: The FAST-MS(DS) Approach at MediaEval 2026},
  author={Jadoon, Aqsa Khan and Rafi, Muhammad},
  booktitle={MediaEval 2026 Working Notes Proceedings},
  year={2026}
}
```

---

# 🙏 Acknowledgment

We thank the MediaEval 2026 NewsImages Challenge organizers for providing the dataset, benchmark framework, and evaluation platform.

---

# 📬 Contact

**Aqsa Khan Jadoon**

GitHub: https://github.com/Aqsa-khan-Jadoon
