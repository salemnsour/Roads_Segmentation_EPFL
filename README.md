# Roads_Segmentation_EPFL


## Overview

This project implements a road segmentation model using deep learning techniques. The goal is to accurately segment road areas in images, which can be useful for applications such as autonomous driving, urban planning, and geographic information systems.

## Table of Contents

- [Installation](#installation)
- [Data Loading & Augmentation](#data-loading--augmentation)
- [Model Architecture](#model-architecture)
- [Loss Functions](#loss-functions)
- [Training](#training)
- [Testing](#testing)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Installation

To run this project, ensure you have the following dependencies installed:
```bash
pip install torch torchvision opencv-python numpy
```
## Data Loading & Augmentation
The project includes functions for loading images and masks, as well as random augmentation techniques to enhance the dataset. Key functions include:

randomHueSaturationValue: Adjusts the hue, saturation, and value of images.
randomShiftScaleRotate: Applies random shifts, scales, and rotations to images and masks.
default_loader: Loads and processes images and their corresponding masks.
Model Architecture
The model is based on a deep learning architecture (e.g., DinkNet152) designed for semantic segmentation tasks. It utilizes convolutional layers with dilation for better feature extraction.

## Loss Functions
To improve model learning and address class imbalance, a combination of Binary Cross-Entropy (BCE) and Dice loss is used. The dice_bce_loss class implements this combined loss function.

## Training
The training process involves setting up the optimizer (Adam), defining the learning rate, and implementing evaluation metrics such as the F1 score. The model can be trained using the optimize method within the provided training frame.

## Testing
The testing phase evaluates the model's performance on unseen data. The TTAFrame class utilizes test time augmentation to improve segmentation results.

## Results
Results can be visualized by saving segmented masks to a specified directory. The project includes functionality to write output masks to files after testing.
and we have reached 0.9205 F1 score and 0.9565 Accuracy

## Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue for discussion.

License
This project is licensed under the MIT License. See the LICENSE file for more information.
