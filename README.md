BERT-Based News Classification

This repository contains a news article classification system built using a fine-tuned BERT model. The goal is to automatically assign news articles to one of four predefined topics. A traditional machine learning model is also included to serve as a comparison point.

What This Project Does

Uses a pre-trained BERT model and fine-tunes it for news classification

Applies tokenisation and padding to prepare text for model input

Trains a multi-class classifier on the AG News dataset

Implements a traditional TF-IDF + Logistic Regression model

Compares deep learning and traditional approaches using evaluation metrics

Data Description

The project is based on the AG News dataset, which contains short news articles collected from various sources.

Categories: World, Sports, Business, Science/Technology

Training samples: ~120,000

Test samples: ~7,600

The dataset is loaded directly using the Hugging Face Datasets library.

Model Setup
BERT Fine-Tuning

Base model: bert-base-uncased

Classification type: multi-class (4 labels)

Token length: 128

Optimiser: AdamW

Learning rate: 2e-5

Batch size: 16

Epochs: 3

The Hugging Face Trainer API is used to manage training and evaluation.

Traditional Baseline

A simpler model is trained using:

TF-IDF feature extraction

Logistic Regression classifier

This helps measure the performance gain achieved by using BERT.

Performance Overview

BERT model accuracy: ~94.7%

Baseline model accuracy: ~91.8%

The transformer-based model performs better across precision, recall, and F1-score, especially for categories with overlapping vocabulary.

Why This Project

This work was completed for an academic coursework assignment to explore the effectiveness of transformer-based models compared to traditional machine learning methods for text classification.
