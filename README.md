Deep Learning from Scratch: Fine-Grained Bird Classification

Overview
This repository contains a deep learning project focused on fine-grained bird species classification, the Challenge is distinguishing 200 visually similar bird species starting from a completely blank 'brain' (no pre-training) without memorizing the limited training data.


Repository Contents

-BaselineNB.ipynb
Establishes the baseline model and performance, using a pretrained ResNet50 model. 

-aml2025-improved-model.ipynb
The main notebook containing the alternative solution. It implements a custom ResNet18-style architecture trained from scratch, along with advanced regularization and augmentation techniques.

-README.md


Assignment
Task: Fine-grained image classification (200 bird species)

Dataset size: ~4,000 images

Constraint: No pretrained weights


Model Architecture
Architecture: Custom ResNet18 with Dropout 
We implemented a Residual Network (ResNet) from scratch to allow deep feature extraction without vanishing gradients. 
Novelty: We injected Dropout (p=0.5) into the final fully connected layers. This is non-standard for ResNets (which usually rely on Batch Norm) but was crucial to prevent our specific model from memorizing the small dataset. 


MixUp augmentation
Instead of showing the model standard images, we blended pairs of images of birds and mixed their labels. 
Why: This prevents the model from being "overconfident" on noisy data and forces it to learn the concept of a bird rather than the specific background of a training image. 
The "Lens": Random Resized Crop 
We replaced standard resizing with aggressive cropping. This acts as an "automatic object detector," forcing the model to recognize a bird by just its head, wing, or tail, rather than relying on the full shape every time. 


Results
Random chance: 0.5%
Simple CNN baseline: ~5–8%
Final model (custom ResNet18): 28.75% Top-1 accuracy
This represents a 57× improvement over random guessing under strict training-from-scratch constraints.







