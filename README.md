## Game Recommendation System on Steam 

# Overview
A game recommendation system created for steam, a well-known video game distribution platform, is presented in this project. The system seeks to improve user engagement and happiness by offering precise and tailored game suggestions by utilizing both content-based filtering and collaborative filtering.


## Features


## Project Overview
Develop an intelligent system to monitor and analyze workplace posture in real-time using deep learning techniques.

## Technologies Used
- Python
- OpenCV
- TensorFlow
- Keras
- PyTorch
- NumPy
- Pandas

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/meCeltic/Machine-learning-Projects/tree/master/Sitting-Posture-Recognition
    ```
2. Navigate to the project directory:
    ```sh
    cd Sitting-Posture-Recognition
    ```
3. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate   # On Windows: venv\Scripts\activate
    ```
4. Install the required packages.

## Usage
1. **Data Preparation**: Place your annotated data in the `data` directory.
2. **Training the Model**:
    ```sh
    model.py
    ```
3. **Real-Time Monitoring**:
    ```sh
    posture_realtime.py
    ```
4. The system will start capturing video from your camera and display real-time posture analysis.

## Model Architecture
The CNN model used for posture detection is designed with the following layers:
- Convolutional layers
- MaxPooling layers
- Fully connected layers
- Softmax activation for output classification

## Data Collection and Preprocessing
- Data was collected from workplace surveillance footage.
- Images were annotated with posture labels.
- Preprocessing steps include resizing, normalization, and splitting into training/validation/test sets.

Training was performed on annotated images with various postures.

## Real-Time Video Processing
OpenCV was used to capture real-time video feed and overlay posture classification results using the trained CNN model.

## Results
The model achieved an accuracy of 90% on the test dataset. Below are some visualizations and example outputs from the real-time monitoring system.
