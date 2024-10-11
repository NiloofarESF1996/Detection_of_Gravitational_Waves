# Detection of Gravitational Waves Using Topological Data Analysis  
**Non-spinning Binary Black Holes Coalescing Event**

## Overview

This project focuses on detecting gravitational waves caused by non-spinning binary black hole mergers through a combination of **simulation**, **topological data analysis (TDA)**, and **machine learning**. Gravitational waves, one of Einstein’s most profound predictions, are emitted by massive events like black hole mergers. In this project, we simulate time series data for gravitational waves, apply topological methods to extract features, and use a machine learning model to classify and detect gravitational wave signals.

### Objective:
The goal is to develop a systematic approach for detecting gravitational waves from non-spinning binary black holes coalescing, using **topological data analysis** to process time series data and a **Support Vector Machine (SVM)** classifier for signal detection.

## Methodology

### 1. Data Simulation
- **2000 samples** of gravitational wave time-series were simulated, each representing a non-spinning binary black hole coalescing event.
- **Systematic noise** was also simulated for 2000 samples, creating a balanced dataset for classification.

### 2. Topological Data Analysis (TDA)
- **Sliding Window Embedding**: We employed the sliding window method to convert the 1-dimensional time series into higher-dimensional feature spaces.
- **Gaussian Kernel**: Applied to smooth out the time series data before embedding.
- **Persistent Homology**: Calculated to measure the shape of the data by computing **Betti curves**. Betti curves represent the topological features of the embedded time series and have been shown to be resistant to noise.
  
### 3. Feature Extraction
- The **Betti Curves** are used as feature vectors for the next step of classification. These curves capture the essential topological features from the gravitational wave signals and allow for effective classification.

### 4. Machine Learning Model
- **Support Vector Machine (SVM)**: The extracted feature vectors (Betti curves) were used as input for the SVM model. The model was trained to distinguish between true gravitational wave signals and noise.
- **Accuracy**: We achieved a maximum accuracy of **97.3%** by varying the signal-to-noise ratio, with the best performance obtained for an embedding dimension of 8 and a time delay of 1.

## Data Processing Workflow

1. **Data Loading**: Simulated time-series data for gravitational wave signals and noise.
2. **Gaussian Smoothing**: Applied Gaussian kernels to reduce noise and enhance signal clarity.
3. **Sliding Window Embedding**: The time series data was embedded into a higher-dimensional space using sliding window techniques.
4. **Persistent Homology**: Computed Betti curves to represent the topological features of the data.
5. **Feature Extraction**: Betti curves served as feature vectors for machine learning.
6. **Classification**: A Support Vector Machine (SVM) was trained and tested to classify gravitational wave signals with high accuracy.

## Notebooks

- **sample_DataSet-TDA.ipynb**: Contains the code for data simulation and the process of generating Betti curves from the gravitational wave and noise data.
- **ML_v5.ipynb**: Includes the machine learning model (SVM) used to classify the signals based on the topological features.

## Results

The project demonstrates that topological data analysis, when combined with machine learning, can be highly effective in detecting gravitational waves. The results show that Betti curves, as feature vectors, are robust against noise, and the SVM classifier can distinguish gravitational wave signals from noise with high accuracy (97.3%).

### Key Achievements:
- **High accuracy** in detecting non-spinning binary black hole coalescing events from noisy data.
- **Robust feature extraction** using Betti curves that are resistant to noise.
- **Efficient classification** of gravitational wave signals using an SVM model.

## How to Use

### Prerequisites:
- Python 3.x
- Libraries: `pandas`, `numpy`, `scikit-learn`, `gudhi` (for topological data analysis), `matplotlib`

### Steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/gravitational-wave-detection.git
