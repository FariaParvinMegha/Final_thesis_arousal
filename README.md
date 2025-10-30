# Final_thesis_arousal
## A Comparison Between Different Stand-Alone and Hybrid Deep Learning Models for Classifying Emotion from EEG Signal
This project compares multiple deep learning models for emotion recognition using EEG signals from the DEAP dataset. It implements CNN, GRU, and a hybrid CNN+LSTM+GRU model to classify emotions into positive, neutral, and negative categories across valence, arousal, dominance, and liking metrics. Feature extraction is performed using Fast Fourier Transform (FFT) on EEG data.

# Table of Contents
- [Introduction](https://github.com/FariaParvinMegha/Final_thesis_arousal/blob/main/README.md#introduction)
- [Features](https://github.com/FariaParvinMegha/Final_thesis_arousal/blob/main/README.md#features)
- [Models](https://github.com/FariaParvinMegha/Final_thesis_arousal/blob/main/README.md#models)
- [Hyperparameters](https://github.com/FariaParvinMegha/Final_thesis_arousal/blob/main/README.md#hyparameters)
- [Evaluation Metrics](https://github.com/FariaParvinMegha/Final_thesis_arousal/blob/main/README.md#evaluation-metrics)
- [Results](https://github.com/FariaParvinMegha/Final_thesis_arousal/blob/main/README.md#Results)
- [Installation Requirements](https://github.com/FariaParvinMegha/Final_thesis_arousal/blob/main/README.md#installation-requirements)
- [Usage](https://github.com/FariaParvinMegha/Final_thesis_arousal/blob/main/README.md#usage)

# Introduction
Emotion recognition is vital for human-computer interaction, healthcare, and affective computing. EEG-based emotion detection provides more reliable signals than facial or speech cues. Deep learning models such as CNNs and RNNs can capture both spatial and temporal EEG features for improved classification accuracy.

# Features
- EEG-Based Emotion Detection: Utilizes the [DEAP dataset](http://eecs.qmul.ac.uk/mmv/datasets/deap/) (32 subjects, 40 signals).
- Feature Extraction: FFT and PSD computed across five EEG frequency bands (delta, theta, alpha, beta, gamma).
- Deep Learning Models: CNN, GRU, and CNN+LSTM+GRU hybrid.
- Multi-Class Emotion Classification: Positive, neutral, negative categories for four emotion metrics.

# Models
| Model  | Description                           | Strength             |
| ------ | ------------------------------------- | -------------------- |
| CNN    | Learns spatial patterns automatically | High accuracy        |
| GRU    | Captures temporal dependencies        | Low loss             |
| Hybrid | Combines CNN, LSTM, GRU               | Balanced performance |

# Hyperparameters
- 50 epochs
- batch size: 256
- optimizer: Adam
- activation functions: ReLU & SoftMax
- callbacks: early stopping & variable learning rate.

# Evaluation Metrics
- Accuracy
- Loss
- Precision
- F1-Score
- Confusion Matrix
- ROC-AUC (AUC ≈ 0.98–0.99).

# Results
| Model  | Accuracy | Precision | F1-Score |
| ------ | -------- | --------- | -------- |
| CNN    | ~93.4%   | ~93.5%    | ~93.4%   |
| GRU    | ~92.8%   | ~93.0%    | ~92.8%   |
| Hybrid | ~92.5%   | ~92.7%    | ~92.5%   |

All models exhibited strong emotion recognition performance, with CNN slightly outperforming others in accuracy, while GRU minimized loss.

# Installation Requirements
- Python 3.x
- Google Colab, Jupyter Notebook or any preferred IDE
- Run the codes cellwise

# Usage 
- Load the Dataset: Import the DEAP dataset into the working directory.
- Run Model Comparisons: Execute the notebook or script to train and test each model on the dataset for each category.
- Evaluate Results: Compare the accuracy and performance of each model to verify the effectiveness of the models.
