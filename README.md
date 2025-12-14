Deep Learning from Scratch: Fine-Grained Bird Classification

Overview
This repository contains a deep learning project focused on fine-grained bird species classification under a strict constraint: no pretrained weights were allowed. The goal was to investigate how far a model trained entirely from scratch can 
go when data is limited and the number of classes is large (200 bird species). The project demonstrates how architecture design, regularization, and advanced data augmentation can significantly reduce overfitting and enable meaningful learning even in data-starved settings.


Repository Contents

BaselineNB.ipynb
Establishes the baseline model and performance. This notebook illustrates the difficulty of the task and shows how naïve approaches severely overfit and perform near random chance.

aml2025-improved-model.ipynb
The main notebook containing the improved solution. It implements a custom ResNet18-style architecture trained from scratch, along with advanced regularization and augmentation techniques.

