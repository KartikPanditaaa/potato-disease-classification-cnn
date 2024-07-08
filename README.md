# Potato Disease Classification Using CNN

This repository contains the code for a machine learning project that classifies potato diseases using a Convolutional Neural Network (CNN). The project utilizes several technologies and frameworks to build, train, and deploy the model, as well as create web and mobile interfaces for user interaction.

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Model Training](#model-training)


## Project Overview
The objective of this project is to accurately classify various potato diseases using images of potato leaves. The core of the project is a Convolutional Neural Network (CNN) implemented using TensorFlow. The dataset is enhanced with data augmentation techniques to improve the model's performance.

## Technologies Used
- **TensorFlow**: For building and training the CNN model.
- **CNN**: A deep learning model specifically designed for image classification tasks.
- **TF Dataset**: A TensorFlow tool for loading and preprocessing datasets.
- **Data Augmentation**: Techniques to artificially increase the diversity of the dataset.

## Setup Instructions
1. **Clone the repository**:
    ```sh
    git clone https://github.com/KartikPanditaaa/potato-disease-classification-cnn.git
    cd potato-disease-classification-cnn
    ```

2. **Install dependencies**:
    - Python dependencies:
      ```sh
      pip install -r requirements.txt
      ```

## Model Training
1. **Prepare the dataset**:
    - Download the dataset and place it in the `data` directory.
    - Run the data preprocessing script:
      ```sh
      python scripts/preprocess_data.py
      ```

2. **Train the model**:
    ```sh
    python scripts/train_model.py
    ```

3. **Evaluate the model**:
    ```sh
    python scripts/evaluate_model.py
    ```




