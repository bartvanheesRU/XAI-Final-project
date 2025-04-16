# XAI Final project

This project focuses on analyzing image attributions and perturbations using pre-trained deep learning models. The analysis includes visualizing attribution maps for original images, naturally perturbed images, and adversarial images. The images that are used are both professional and wildlive images of wolves. 

## Table of Contents

1. [Setup](#setup)
2. [Usage](#usage)
3. [Models](#models)
4. [Attribution Methods](#attribution-methods)
5. [Natural Perturbations](#natural-perturbations)
6. [Adversarial Images](#adversarial-images)
7. [Results](#results)

## Setup

To run this project, you need to have the following dependencies installed:


1. pip install torch torchvision captum matplotlib numpy pillow torchattacks.
2. torch and torchvision: Provide the core functionality for working with tensors and pre-trained models.
3. captum: Used for model interpretability, specifically for computing attributions.
4. matplotlib: Used for plotting and visualizing the results.
numpy: Provides support for numerical operations.
5. pillow: Used for opening and manipulating images.
6. torchattacks: Provides implementations of adversarial attacks, such as FGSM.



additionally make sure that the imagenet_classes.json file and the images are in your working directory.  

## Models
The following pre-trained modesl are used for analysis:

1. ResNet-50: A widely used convolutional neural network.
2. VGG-16: A deep convolutional network known for its simplicity.
3. DenseNet-121: A densely connected convolutional network.

## Attribution Methods
Two attribution methods are used to visualize the importance of different regions in the images:

1. Saliency (Vanilla Gradient): Computes the gradient of the output with respect to the input image.
2. Integrated Gradients: Computes the integral of gradients with respect to input features along the path from a baseline to the input.

## Natural Perturbations
To analyze natural perturbations, the code includes modifications to apply slight transformations to the images, such as rotations or noise, before computing attributions.

## Adversarial Images
Adversarial images are generated using the Fast Gradient Sign Method (FGSM). The code includes steps to apply FGSM to the input images and visualize the resulting attribution maps.

## Results
The results include visualizations of:

Original images with their predicted labels and scores.
Attribution maps for original, naturally perturbed, and adversarial images.
