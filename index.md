---
layout: default
title: ICME 2025 Grand Challenge | JND Prediction for 3D Point Cloud Compression
---

# ICME 2026 Grand Challenge
## Perceptual Just Noticeable Difference (JND) Modeling for 3D Point Cloud Compression

<nav>
  <a href="#home">Home</a> •
  <a href="#introduction">Introduction</a> •
  <a href="#dataset">Dataset</a> •
  <a href="#tasks">Tasks</a> •
  <a href="#evaluation">Evaluation</a> •
  <a href="#submission">Submission</a> •
  <a href="#dates">Challenge Dates</a> •
  <a href="#organizers">Organizers</a> •
  <a href="#contact">Contact</a>
</nav>

---

<a id="home"></a>
## Home

**Challenge Theme:** Human-centric perceptual modeling for point clouds: **JND prediction** under compression distortions.  
**Keywords:** Point Cloud Compression, Perceptual Quality, JND, PKU-JND, G-PCC, Human Visual System

> 🔔 *This page is a template for ICME 2025. Dates and platform links will be updated if the organizing committee revises the schedule.*

---

<a id="introduction"></a>
## Introduction

Point clouds are a fundamental 3D representation widely used in immersive media, autonomous driving, digital twins, AR/VR, and telepresence. In practice, point cloud data often undergo compression, transmission, and rendering under strict bandwidth/storage/compute constraints, which inevitably introduces perceptual quality degradation. Accurate perceptual quality assessment is therefore critical for user experience and reliable downstream applications. 

**Just Noticeable Difference (JND)** describes the minimum distortion level at which degradation becomes perceptible to human observers. JND modeling enables perceptually optimized compression by removing imperceptible redundancies while preserving visually critical information. However, point cloud JND modeling is challenging due to irregular spatial distributions, varying densities, complex geometry, and rich attributes (e.g., color), and because distortions can be content-dependent across geometry and attributes. :contentReference[oaicite:5]{index=5}

To advance research in this area, we introduce **PKU-JND**, a large-scale benchmark dedicated to JND measurement for point cloud compression, and host this Grand Challenge to encourage robust JND prediction methods and fair comparison under a standardized evaluation protocol. :contentReference[oaicite:6]{index=6}

---

<a id="dataset"></a>
## Dataset: PKU-JND

**PKU-JND** is the first large-scale benchmark dataset for **JND measurement in point cloud compression**. It is built via carefully designed subjective experiments, aiming to comprehensively capture human perceptual sensitivity to point cloud distortions. :contentReference[oaicite:7]{index=7}

**Key statistics (from proposal):**
- **230** reference point cloud models across **5** representative content categories :contentReference[oaicite:8]{index=8}  
- Distorted samples generated using **MPEG G-PCC** codec:  
  - **5,750** geometry-distorted samples  
  - **7,130** attribute-distorted samples :contentReference[oaicite:9]{index=9}  
- Subjective annotation spans **5 months**, conducted in **two phases**, involving **20–31** participants, with rigorous post-processing (statistics + outlier detection) for reliability. :contentReference[oaicite:10]{index=10}

> 📦 **Data download / access**  
> - Training set: *(to be released)*  
> - Validation set: *(to be released)*  
> - Test set: *(evaluation-only / hidden labels)*  
>
> ✅ Put your actual dataset links here once ready.

---

<a id="tasks"></a>
## Tasks

Participants are invited to develop algorithms to **predict subjective JND thresholds** for compressed point clouds, with a focus on:
- **Geometry JND prediction**
- **Attribute (color/texture) JND prediction**
- Unified modeling that aligns predictions with **human perceptual thresholds**

The goal is to improve human-centric perceptual modeling and facilitate perceptually optimized point cloud compression frameworks. :contentReference[oaicite:11]{index=11}

---

<a id="evaluation"></a>
## Evaluation

Submissions are evaluated on a held-out test set using correlation-based and error-based metrics between predicted JND values and subjective annotations. :contentReference[oaicite:12]{index=12}

Let the subjective JND score be \( s_i \) and the predicted score be \( \hat{s}_i \) for \( i=1,\dots,N \). :contentReference[oaicite:13]{index=13}

**Metrics:**
1. **PLCC (Pearson Linear Correlation Coefficient)** :contentReference[oaicite:14]{index=14}  
2. **SRCC (Spearman Rank-Order Correlation Coefficient)** :contentReference[oaicite:15]{index=15}  
3. **KRCC (Kendall Rank Correlation Coefficient)** :contentReference[oaicite:16]{index=16}  
4. **RMSE (Root Mean Squared Error)** :contentReference[oaicite:17]{index=17}  

**Final leaderboard score:**  
\[
\text{Score} = \frac{\text{PLCC} + \text{SRCC}}{2}
\]
Final rankings are determined by **Score**, while PLCC, SRCC, KRCC, and RMSE are all reported. :contentReference[oaicite:18]{index=18}

**Reproducibility & fairness:**
- An **official evaluation script** will be released to compute all metrics and ensure reproducibility. :contentReference[oaicite:19]{index=19}  
- Participants must use **only the official training data**. Any external data usage (pretraining/fine-tuning/distillation/model selection) is **strictly prohibited**. :contentReference[oaicite:20]{index=20}  

---

<a id="submission"></a>
## Submission

Participants must submit **prediction results** for the official test set following the provided **JSON format**, and all evaluations will be performed using the official evaluation script. :contentReference[oaicite:21]{index=21}

**Submission platform:** *(to be announced)* :contentReference[oaicite:22]{index=22}  
**Daily limit:** up to **3 submissions per team per day**. :contentReference[oaicite:23]{index=23}

> ✅ Put your actual competition platform link here (e.g., CodaLab / Kaggle / EvalAI / internal server).

---

<a id="dates"></a>
## Challenge Dates

> ⚠️ The following dates are taken from the proposal and may be updated by organizers if necessary. :contentReference[oaicite:24]{index=24}  
> All deadlines are at **11:59 PM UTC** on the corresponding day unless otherwise noted. :contentReference[oaicite:25]{index=25}

| Event | Date |
|---|---|
| Registration Open | 2026-02-15 |
| Training Data Release | 2026-03-10 |
| Challenge Result Submission Deadline | 2026-04-25 |
| Challenge Technical Paper Submission Deadline | 2026-05-10 |
| Final Decisions | 2026-05-15 |
| Camera Ready Submission Deadline | 2026-05-25 |

---

<a id="organizers"></a>
## Organizers

- **Liang Xie**, Guangdong University of Technology, Guangzhou, China (LXie5201@outlook.com) :contentReference[oaicite:26]{index=26}  
- **Wei Gao**, Peking University, Shenzhen, China (gaowei262@pku.edu.cn) :contentReference[oaicite:27]{index=27}  
- **Ge Li**, Peking University, Shenzhen, China (geli@pku.edu.cn) :contentReference[oaicite:28]{index=28}  
- **Yanting Li**, Guangdong University of Technology, Guangzhou, China (1209847234@qq.com) :contentReference[oaicite:29]{index=29}  

---

<a id="contact"></a>
## Contact

For questions, please contact the organizers via email:

- LXie5201@outlook.com  
- gaowei262@pku.edu.cn  
- geli@pku.edu.cn  
- 1209847234@qq.com  

---

© ICME Grand Challenge | JND Prediction for 3D Point Cloud Compression
