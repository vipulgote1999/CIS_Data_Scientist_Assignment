# Food-101 Image Classification using InceptionV3

## Overview

This project implements a deep learning-based image classification model using InceptionV3 to classify food images from the Food-101 dataset. The training process is tracked using Weights & Biases (WandB) for better visualization and monitoring.

## Features

- Uses InceptionV3 as the backbone model
- Implements data augmentation for improved generalization
- Tracks training progress using Weights & Biases (WandB)
- Uses EarlyStopping and ReduceLROnPlateau for training optimization
- Saves the best model based on validation performance

## Dataset

The model is trained on the Food-101 dataset, which contains 101 food categories with 101,000 images.

Dataset is downloaded and loaded using tensorflow.keras.preprocessing.image_dataset_from_directory.

## Installation

To run this project, install the required dependencies:
```
pip install tensorflow wandb numpy pandas matplotlib
```

## Setup WandB

Before running the script, set up Weights & Biases:
```
wandb login
```
## Training the Model

Run the above notebook to train model

## Key Hyperparameters:

Batch Size: 32
Image Size: (224, 224)
Learning Rate: 0.001 (reduced on plateau)
Epochs: 10 (can be adjusted)

## Model Architecture

Base Model: InceptionV3 (pretrained on ImageNet)
Custom Fully Connected Layers:
Flatten
Dense(512, ReLU, Dropout(0.5))
Dense(101, Softmax)
  
## Model Evaluation

The model is evaluated based on:

- Accuracy
- Top-3 Categorical Accuracy

## Validation Loss & Accuracy Trends

## Visualization

You can view training results on WandB:
```
wandb.init(project='food101-classification')
```
wandb link(https://wandb.ai/existence/CIS_image_classification_1743570321.36446/runs/v9hjp510)

## Results

Final model achieves 84% accuracy on the validation dataset.

Training logs and visualizations are available in WandB.

##Author

Vipul Gote
Contact: vipulgote4@gmail.com

## License
This project is licensed under the MIT License.
