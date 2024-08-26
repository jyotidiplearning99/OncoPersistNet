### OncoPersistNet
## Overview
OncoPersistNet is a deep learning framework developed to classify persister and non-persister cancer cells using single-cell RNA sequencing (scRNA-seq) data. This repository provides the codebase for a hybrid Convolutional Neural Network (CNN) and Recurrent Neural Network (RNN) model, designed to capture both spatial and temporal features in gene expression data, aiding in the understanding of cancer treatment resistance.

Table of Contents
Introduction
Features
Installation
Usage
Data Preprocessing
Model Architecture
Evaluation Metrics
Results
Future Work
Contributing
License
Introduction
Cancer is a complex disease with diverse cell populations within tumors. Among these, persister cells are a subset known for their resilience to treatment, contributing to cancer recurrence. OncoPersistNet aims to accurately classify these persister cells, offering insights into treatment resistance and potential new therapeutic targets.

Features
Hybrid Model: Combines the strengths of CNN and RNN to handle both spatial and sequential data features.
Data Preprocessing: Includes imputation, normalization, and Principal Component Analysis (PCA) for optimal model performance.
Comprehensive Evaluation: Utilizes various metrics, including accuracy, precision, recall, F1-score, and ROC-AUC.
Transfer Learning: Capable of generalizing to independent datasets, demonstrating robust performance across different cancer types.

Usage
To train and evaluate the model, follow these steps:

Prepare Your Data: Ensure your scRNA-seq data is formatted according to the guidelines in the data/ directory.
Run Preprocessing: Use the provided scripts in the preprocessing/ folder to preprocess your data.

Data Preprocessing
The data preprocessing pipeline includes the following steps:

Imputation: Handles missing data using mean imputation.
Normalization: Scales gene expression data using min-max normalization.
Dimensionality Reduction: Applies PCA to reduce data dimensionality while preserving key variance.
Refer to the preprocessing/ directory for detailed scripts.

Model Architecture
OncoPersistNet employs a hybrid CNN-RNN architecture:

Conv1D Layers: Capture spatial gene expression patterns.
LSTM Layers: Model temporal dependencies in gene expression over time.
Dense Layers: Classify cells as persister or non-persister based on learned features.
The full architecture is defined in model.py.

Evaluation Metrics
The model's performance is evaluated using:

Accuracy
Precision and Recall
F1-Score
ROC-AUC


Results
The model achieved high accuracy and robust performance across multiple datasets, demonstrating its potential for aiding in cancer research and therapy development. Detailed results can be found in the results/ folder.

Future Work
Future improvements to OncoPersistNet could include:

Incorporating attention mechanisms for better feature extraction.
Expanding the model to classify persister cells in other cancer types.
Enhancing model interpretability using explainable AI techniques.
