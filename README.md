# Animal Classification Using CNN

## Overview
This project implements an animal classification model using Convolutional Neural Networks (CNN) in TensorFlow/Keras. It uses the "Animals with Attributes 2" dataset from Kaggle to train two different CNN architectures for comparison. The models are evaluated on various conditions, including manipulated images and color stability applications.

## Dataset
The dataset is downloaded from Kaggle using `kagglehub` and contains images of the following animals:
- Collie
- Dolphin
- Elephant
- Fox
- Moose
- Rabbit
- Sheep
- Squirrel
- Giant Panda
- Polar Bear

## Project Workflow
1. **Data Preprocessing:**
   - Download dataset using `kagglehub`
   - Load and filter images to a maximum of 650 per class
   - Resize images to 128x128 pixels
   - Normalize pixel values
   
2. **Dataset Splitting:**
   - Images are split into training (70%) and testing (30%) sets
   - Labels are encoded and converted into categorical format

3. **Data Augmentation:**
   - Apply transformations such as rotation, width/height shifts, shear, zoom, and horizontal flips

4. **Model Architectures:**
   - `build_model()`: Basic CNN with three convolutional layers
   - `build_alternate_model()`: Enhanced CNN with Batch Normalization and L2 regularization

5. **Training:**
   - Both models are trained using augmented images
   - Trained models are saved as `animal_classifier.h5` and `alternate_animal_classifier.h5`

6. **Evaluation:**
   - Models are evaluated on the original test set
   - Performance is tested on manipulated images (brightness/contrast changes)
   - Color stability corrections are applied and evaluated

## Results
- **Original Test Set Accuracy**: The accuracy on unmodified images
- **Manipulated Test Set Accuracy**: The accuracy on images with brightness and contrast variations
- **Color Stability Applied Test Set Accuracy**: The accuracy after color constancy adjustments

## Conclusion
This project demonstrates how CNNs can effectively classify animal images while addressing robustness challenges using data augmentation, brightness/contrast adjustments, and color constancy techniques.

