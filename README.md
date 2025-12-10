# Evidential Uncertainty Modeling for circRNA–Disease Prediction  
### CSC 8851 — Deep Learning (Fall 2025)  
### Final Project Submission  
**Author:** Akshat Namdeo  

---

## Project Overview

This repository contains all code and materials for the course project **“Evidential Uncertainty Modeling for circRNA–Disease Association Prediction”**, completed as part of **CSC 8851: Deep Learning**.

The project extends relational graph neural networks (R-GCNs) with evidential modeling to quantify **epistemic uncertainty** in biomedical link prediction tasks.  
We construct a heterogeneous biological graph (circRNAs, diseases, genes), train a relational GNN for link prediction, and attach an evidential head that outputs **Dirichlet evidence** for calibrated confidence estimation.

The work includes:

- A fully reproducible preprocessing pipeline  
- R-GCN training (Stage A)  
- Evidential uncertainty modeling (Stage B)  
- Evaluation of calibration, uncertainty trends, and biological case studies  
- A CVPR-style final project paper + supplementary material

---

## Repository Structure

### **1. `preprocessing/Preprocessing.ipynb`**  
Builds the heterogeneous circRNA–disease–gene graph used for all experiments.  
Implements:
- circRNA & gene loading  
- DOID normalization  
- Constructing CC, CD, CG, DD relations  
- Needleman–Wunsch sequence alignment for circRNA similarity  
- Top-K similarity graph  
- Final graph dictionary `G`

### **2. `training/Experiment_1.ipynb`**  
Main training and inference notebook.  
Contains:
- R-GCN encoder (Stage A)  
- DistMult head baseline  
- Evidential head training (Stage B)  
- Calibration experiments  
- Uncertainty-vs-structure analysis  
- Case studies for BC, HCC, CRC, GBM
  
---

## Project Summary

- We extend a relational GNN with an evidential uncertainty head.  
- Uncertainty correlates strongly with structural graph support.  
- Case studies illustrate how low-vacuity predictions align with known biology, while high-vacuity predictions correspond to unverified or structurally unsupported associations.  
- The approach improves interpretability without modifying the encoder architecture.

---

## Environment & Setup

This project will include a fully documented `environment.yml` or `requirements.txt` once final module versions are frozen.

---

## Important Note

**The finalized code modules, complete environment specifications, and final paper (with supplementary sections) will be uploaded shortly.**  
These will include:
- Clean, modular versions of Stage A (R-GCN) and Stage B (EPN)  
- Reproducible training scripts  
- Additional ablation studies and plots  
- Final PDF (4-page paper + references + supplementary)

---

## License

This project is submitted for academic evaluation only and is not licensed for commercial use.

---
