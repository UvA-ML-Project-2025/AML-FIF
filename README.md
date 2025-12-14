Deep Learning from Scratch: Fine-Grained Bird Classification

Overview
This repository contains a deep learning project focused on fine-grained bird species classification, the Challenge is distinguishing 200 visually similar bird species starting from a completely blank 'brain' (no pre-training) without memorizing the limited training data.


Repository Contents

BaselineNB.ipynb
Establishes the baseline model and performance, using a pretrained ResNet50 model. 

aml2025-improved-model.ipynb
The main notebook containing the alternative solution. It implements a custom ResNet18-style architecture trained from scratch, along with advanced regularization and augmentation techniques.


Task: Fine-grained image classification (200 bird species)
Dataset size: ~4,000 images
Constraint: No pretrained models or external data


Model Architecture

Custom ResNet18 implemented from scratch
Residual connections for stable deep learning
Dropout (p = 0.5) added to fully connected layers to reduce memorization

Regularization & Augmentation

MixUp augmentation to reduce overconfidence and improve robustness
Random Resized Crop to prevent background memorization
Label smoothing for better generalization

Results

Random chance: 0.5%
Simple CNN baseline: ~5–8%
Final model (custom ResNet18): 28.75% Top-1 accuracy
This represents a 57× improvement over random guessing under strict training-from-scratch constraints.







