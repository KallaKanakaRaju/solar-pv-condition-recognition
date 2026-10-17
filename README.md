# Image-Based Solar PV Condition Recognition Using Handcrafted Features

## Overview

This repository contains the implementation and experimental results of a machine learning framework for image-based solar photovoltaic (PV) panel condition recognition. The study investigates the predictive performance and computational efficiency of multiple machine learning classifiers using handcrafted image features.

The framework extracts statistical, color, texture, and edge-based features from solar panel images and evaluates different classifiers to identify panel conditions. The study emphasizes a comparative analysis of classification performance, computational cost, and model size.

## Dataset

The dataset used in this study is the **Solar Panel Images** dataset available on Kaggle.

**Dataset link:** https://www.kaggle.com/datasets/pythonafroz/solar-panel-images

The dataset contains solar panel images representing six condition categories:

| Class | Description |
|---|---|
| Bird-drop | Solar panels affected by bird droppings |
| Clean | Clean solar panel surfaces |
| Dusty | Solar panels covered with dust |
| Electrical-damage | Solar panels exhibiting electrical damage |
| Physical-Damage | Solar panels exhibiting physical damage |
| Snow-Covered | Solar panels covered with snow |

### Dataset Preparation

For the experiments reported in this study, 885 images were used. The data were divided into training, validation, and testing subsets.

| Subset | Number of images |
|---|---:|
| Training | 619 |
| Validation | 133 |
| Testing | 133 |
| **Total** | **885** |

The dataset was divided using a stratified splitting procedure with random seed 42.

**Note:** The dataset is not included in this repository. Please download it from Kaggle and review the dataset's licensing and usage terms before using or redistributing its images.

## Methodology

The proposed framework consists of the following stages:

1. **Image loading:** Load the solar panel images and their corresponding class labels.
2. **Feature extraction:** Extract handcrafted image features describing color, brightness, texture, sharpness, and edge characteristics.
3. **Feature analysis:** Analyze the extracted features using statistical analysis and principal component analysis (PCA).
4. **Model training:** Train and evaluate multiple machine learning classifiers.
5. **Performance evaluation:** Compare predictive performance and computational efficiency using classification metrics and inference measurements.

### Handcrafted Features

A total of 29 handcrafted features are used in the experiments, including:

- **Color features:** RGB and HSV channel statistics.
- **Brightness features:** Mean, median, and standard deviation of brightness.
- **Texture features:** Entropy and gray-level co-occurrence matrix (GLCM) statistics.
- **Edge and gradient features:** Edge density and gradient statistics.
- **Sharpness features:** Image sharpness measurements.

These features provide a compact representation of solar panel appearance without requiring a deep neural network for feature extraction.

### Machine Learning Models

The study compares the following classifiers:

- CatBoost
- LightGBM
- Histogram-based Gradient Boosting (HistGradientBoosting)
- Multilayer Perceptron (MLP)
- K-Nearest Neighbors (KNN)

## Evaluation Metrics

The models are compared using the following metrics:

- Accuracy
- Macro-F1 score
- Weighted-F1 score
- Balanced accuracy
- Class-wise performance
- Training time
- Inference latency per image
- Model size

These metrics enable evaluation of both predictive performance and computational efficiency.

## Experimental Results

The test-set results show that HistGradientBoosting achieved the highest accuracy of **71.43%** and the highest balanced accuracy of **64.15%** among the five evaluated classifiers.

LightGBM achieved the highest macro-F1 score of **63.65%**.

The results demonstrate the trade-offs between classification performance and computational requirements when using handcrafted features for solar PV condition recognition.

Detailed numerical results, tables, and figures will be provided in the repository's results directory.



