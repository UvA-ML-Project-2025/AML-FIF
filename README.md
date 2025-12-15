Deep Learning from Scratch: Fine-Grained Bird Classification

Overview:

This repository contains a deep learning project focused on fine-grained bird species classification, the Challenge is distinguishing 200 visually similar bird species starting from a completely blank 'brain' (no pre-training) without memorizing the limited training data.


Repository Contents:

├── BaselineNB.ipynb:
Establishes the baseline model and performance, using a pretrained ResNet50 model. 

├── aml2025-improved-model.ipynb:
The main notebook containing the alternative solution. It implements a custom ResNet18-style architecture trained from scratch, along with advanced regularization and augmentation techniques.

└── README.md



Assignment:

├── Task: Fine-grained image classification (200 bird species)

├── Dataset size: ~4,000 images

└── Constraint: No pretrained weights


Baseline Model: ResNet50
ResNet50 is a 50-layer deep convolutional neural network introduced in 2015 and designed for image recognition. It uses residual (skip) connections that make training deep networks stable and effective. The model was originally trained on ImageNet, has 25.6 Million parameters, and achieves a 76.0% top-1 accuracy on ImageNet.

Test set accuracy: 46.33%

Alternative model: Custom ResNet18 with Dropout
Our alternative model is a custom ResNet18 convolutional neural network for bird image classification. To improve generalization on a small dataset, Dropout (p=0.5) was added to the final fully connected layers. Training used MixUp augmentation, where images and labels of different bird were blended, encouraging the model to learn shared visual characteristics of birds rather than memorizing species-specific backgrounds. Additionally, aggressive Random Resized Cropping was applied, forcing the model to recognize birds from partial cues such as the head, wing, or tail instead of relying on the full bird silhouette.

Test set accuracy: 25.18%


Conclusion: We are trading accuracy for data independence. Our model proves learning is possible without reliance on massive external datasets, but with lower performance. 






