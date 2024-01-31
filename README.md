# Long-Tailed Image Classification using ConvNeXt-Tiny Model

This project explores the application of the ConvNeXt-Tiny model for image classification on the long-tailed Caltech-101 dataset. Our primary focus is to address the challenges posed by imbalanced datasets and improve classification accuracy for small sample categories.

## Overview

The ConvNeXt-Tiny model, originally inspired by the ConvNeXt architecture, is adapted to work efficiently with limited computational resources. This project incorporates various techniques to tackle overfitting and data imbalance, enhancing model performance on the Caltech-101 dataset.

## Dataset

The Caltech-101 dataset comprises approximately 9000 images across 101 categories, exhibiting a long-tailed distribution. The dataset is divided into 70% for training, 15% for validation, and 15% for testing to maintain the distribution's integrity.

## Methodology

- **Weighted Random Sampling:** To manage class imbalance, each category is assigned weights inversely proportional to its frequency.
- **Data Augmentation:** We use online augmentation techniques such as random flipping, rotation, cropping, scaling, and color adjustments.
- **Mixup Technique:** This involves linear interpolation of image pairs to generate additional training data.
- **Exponential Moving Average (EMA):** To stabilize training and reduce loss jitter.
- **Group L2 Weight Decay:** Implemented to reduce model overfitting.
- **Cosine Annealing Learning Rate Scheduling:** This strategy involves varying the learning rate in a cosine function pattern to optimize training.

## Metrics

Model performance is evaluated using Weighted F1 Score, Matthew’s Correlation Coefficient (MCC), and Cohen’s Kappa Score to ensure a fair assessment across imbalanced classes.

## Results

Our comprehensive approach led to significant improvements in handling long-tailed distribution challenges. The use of weighted random sampling, advanced data augmentation techniques, and optimization strategies like EMA and cosine annealing collectively enhanced the model's ability to generalize across various categories.

## Transfer Learning

We further explored transfer learning by initializing our model with weights pre-trained on the ImageNet-11k dataset, leading to an even higher classification accuracy.

## Repository Structure

- `model/`: Contains the implementation of the ConvNeXt-Tiny model.
- `data/`: Scripts for data preprocessing and augmentation.
- `training/`: Training scripts including the application of various techniques.
- `results/`: Stored results and model performance metrics.
- `utils/`: Utility functions used across the project.

## Usage

Detailed instructions on how to set up the environment, preprocess the data, and train the model are provided in respective directories.

## Acknowledgments

This project was developed by Renghe Tang and Weijia Lyu at the University of British Columbia. We thank the authors of the ConvNeXt model and the Caltech-101 dataset for making their resources available.

## References

- [1] Marina Sokolova and Guy Lapalme. "A systematic analysis of performance measures for classification tasks."
- [2] Davide Chicco, et al. "The Matthews correlation coefficient (MCC) is more informative than Cohen’s kappa."
- [3] Jean Carletta. "Assessing agreement on classification tasks: the kappa statistic."

---

For more detailed information, refer to our paper "Long-Tailed Image Classification based on ConvNeXt-Tiny Model".
