# 3D Genome Structure Reconstruction of *E. coli* using Machine Learning

This repository contains the code, data, and results for a project that compares two deep learning models—REACH-3D and TECH-3D—for reconstructing the 3D structure of the *E. coli* genome from Hi-C data.

## 📁 Repository Structure

- `notebooks/`: Jupyter notebooks for model training and evaluation
  - `REACH3D.ipynb`: Unsupervised training of REACH-3D on experimental Hi-C data
  - `TECH3D_StrucGen.ipynb`: Generator for synthetic 3D structures and simulated Hi-C matrices
  - `TECH3D_Training.ipynb`: Supervised training of TECH-3D using synthetic data
- `data/`: Input datasets
  - `hic_experimental/`: Experimental Hi-C data e.g., from [Lioy et al., 2018](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE107301)
  - `tech3d_train_set/`: Synthetic training dataset
  - `tech3d_test_set/`: Synthetic test dataset
- `models/`: Pretrained TECH-3D model checkpoints
- `predictions/`: Predicted 3D coordinates for both models
  - `reach3d/`: REACH-3D predictions
  - `tech3d/`: TECH-3D predictions
- `figures/`: Loss curves and visualization of predictions
- `requirements.txt`: Python dependencies for running the notebooks

## 🧪 Models

### [REACH-3D](https://arxiv.org/abs/1811.09619)
An unsupervised autoencoder with LSTM layers, trained directly on experimental Hi-C matrices.

### [TECH-3D](https://www.biorxiv.org/content/10.1101/2021.12.15.472387v1)
A supervised model trained on synthetic Hi-C/structure pairs using a bidirectional LSTM with a three-part loss function (biological smoothness, structural correlation, distance accuracy).

## 📦 Installation

Create a virtual environment and install dependencies:
```bash
pip install -r requirements.txt
