# Potato Disease Classification Using CNN

This repository contains the code for a machine learning project that classifies potato diseases using a Convolutional Neural Network (CNN). The project utilizes several technologies and frameworks to build, train, and deploy the model, as well as create web and mobile interfaces for user interaction.

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Model Training](#model-training)
- [Model Serving](#model-serving)
- [Web Application](#web-application)
- [Mobile Application](#mobile-application)
- [Deployment](#deployment)

## Project Overview
The objective of this project is to accurately classify various potato diseases using images of potato leaves. The core of the project is a Convolutional Neural Network (CNN) implemented using TensorFlow. The dataset is enhanced with data augmentation techniques to improve the model's performance.

## Technologies Used
- **TensorFlow**: For building and training the CNN model.
- **CNN**: A deep learning model specifically designed for image classification tasks.
- **TF Dataset**: A TensorFlow tool for loading and preprocessing datasets.
- **Data Augmentation**: Techniques to artificially increase the diversity of the dataset.
- **Fast API**: For creating a web API to interact with the model.
- **TF Serving**: For serving the trained model.
- **React.js**: For building the web interface.
- **React Native**: For developing the cross-platform mobile application.
- **Google Cloud Platform (GCP)**: For deploying the application and hosting the services.

## Setup Instructions
1. **Clone the repository**:
    ```sh
    git clone https://github.com/your-username/potato-disease-classification-cnn.git
    cd potato-disease-classification-cnn
    ```

2. **Install dependencies**:
    - Python dependencies:
      ```sh
      pip install -r requirements.txt
      ```
    - Node.js dependencies for web and mobile apps:
      ```sh
      cd web-app
      npm install
      cd ../mobile-app
      npm install
      ```

3. **Configure GCP**:
    - Set up a GCP project and enable necessary APIs.
    - Configure authentication and environment variables for GCP services.

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

## Model Serving
1. **Export the model**:
    ```sh
    python scripts/export_model.py
    ```

2. **Serve the model with TensorFlow Serving**:
    ```sh
    docker run -p 8501:8501 --name=tf_serving \
      --mount type=bind,source=/path/to/exported/model,target=/models/potato_model \
      -e MODEL_NAME=potato_model -t tensorflow/serving
    ```

## Web Application
1. **Start the Fast API server**:
    ```sh
    uvicorn api.main:app --reload
    ```

2. **Run the React.js web application**:
    ```sh
    cd web-app
    npm start
    ```

## Mobile Application
1. **Start the React Native app**:
    ```sh
    cd mobile-app
    npm start
    ```

## Deployment
1. **Deploy the API and web application to GCP**.
2. **Configure CI/CD pipelines for continuous deployment**.


