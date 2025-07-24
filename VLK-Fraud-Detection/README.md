# Transaction Anomaly Detection

A comprehensive machine learning project for detecting anomalous transactions using multiple unsupervised learning approaches. This project was provided to me via Van Lanschot Kempen as a case study day in EBT University day 2025.

## Project Overview

This project implements and compares various anomaly detection algorithms on unlabeled transaction data to identify potentially fraudulent or unusual transaction patterns. The analysis combines dimensionality reduction techniques with state-of-the-art anomaly detection methods.

## Key Features

- **Multiple Anomaly Detection Algorithms**: Implements K-Means clustering, One-Class SVM, Isolation Forest, and Deep SVDD (neural network-based)
- **Dimensionality Reduction**: Compares PCA and t-SNE for data visualization and feature reduction
- **GPU Acceleration**: Utilizes Apple Metal Performance Shaders (MPS) for neural network training on M1/M2 Macs
- **Comprehensive Visualization**: Interactive plots showing anomaly distributions in reduced dimensional space

## Algorithms Implemented

### Traditional Methods
- **K-Means Clustering**: Identifies anomalies as points distant from cluster centers
- **One-Class SVM**: Creates decision boundaries around normal transaction patterns
- **Isolation Forest**: Tree-based ensemble method for isolating anomalies

### Neural Network Approach
- **Deep SVDD**: Autoencoder-based deep learning model for anomaly detection
- Trained with PyTorch and Apple Metal GPU acceleration

## Dimensionality Reduction

- **Principal Component Analysis (PCA)**: Linear dimensionality reduction preserving maximum variance
- **t-SNE**: Non-linear manifold learning for better visualization of complex transaction patterns

## Results

The project successfully identifies approximately 100 anomalous transactions from a dataset of ~200,000 transactions using optimized contamination parameters. Isolation Forest and Deep SVDD showed the most promising results for this dataset.

## Technical Stack

- **Python 3.12**
- **scikit-learn**: Traditional ML algorithms
- **PyTorch**: Neural network implementation with MPS support
- **NumPy/Pandas**: Data manipulation
- **Matplotlib**: Visualization

## Performance

- Leverages Apple Silicon GPU acceleration for neural network training
- Optimized hyperparameters for balanced anomaly detection (targeting ~0.05% anomaly rate)
- Efficient processing of high-dimensional transaction features
