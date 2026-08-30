# Driver Drowsiness & Distraction Detection using Custom CNN

A Deep Learning project that detects driver behavior from camera frames using a **Custom Convolutional Neural Network (CNN)** built from scratch in PyTorch.

## Project Overview

This project classifies driver behavior into five categories using images extracted from recorded driving videos. The model is trained on a self-recorded dataset and implemented entirely in PyTorch without using any pre-trained backbone.

## Classes

- Normal
- Phone
- Drinking
- Sleeping
- Distraction

## Model

**Architecture:** Custom CNN

Features:
- 5 Convolution Blocks
- Batch Normalization
- ReLU Activation
- Max Pooling
- Adaptive Average Pooling
- Dropout Regularization
- Fully Connected Classifier

## Dataset

- Self-recorded driver dataset
- Frames extracted from 1080p videos
- Resized to **854 Ã— 480**
- Stratified **70 / 15 / 15** split
- Total classes: **5**

> Dataset is not included in this repository due to size limitations.

## Training Configuration

| Parameter | Value |
|-----------|-------|
| Framework | PyTorch |
| Optimizer | AdamW |
| Learning Rate | 1e-4 |
| Loss | Cross Entropy + Label Smoothing |
| Epochs | 20 |
| Batch Size | 16 |
| Mixed Precision | Yes (AMP) |
| Early Stopping | Yes |

## Results

| Metric | Score |
|---------|------:|
| Best Validation Accuracy | **82.61%** |
| Best Validation Macro F1 | **82.47%** |

## Repository Structure

```text
.
â”œâ”€â”€ train.ipynb
â””â”€â”€ README.md
```

## Requirements

```bash
pip install torch torchvision pandas numpy matplotlib seaborn scikit-learn tqdm pillow
```

## Run

Open the notebook and execute all cells sequentially.

```bash
jupyter notebook train.ipynb
```


