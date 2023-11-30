# DeepFake Voice Recognition

## Overview

Welcome to the DeepFake Voice Recognition project repository! This project focuses on utilizing Mel-Frequency Cepstral Coefficients (MFCC) to extract features from audio samples and employs the Random Forest algorithm for the classification of voices into fake and real categories. The primary goal is to develop an effective tool for detecting deepfake voices in audio recordings.

## Features

- **MFCC Feature Extraction:** The project leverages MFCC to capture the spectral characteristics of audio signals, providing a robust representation for voice features.

- **Random Forest Classification:** The classification model is built using the Random Forest algorithm, known for its versatility and effectiveness in handling complex datasets.

## Getting Started

Follow these steps to get the project up and running on your local machine:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/DeepFake-Voice-Recognition.git

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt

3. **Dataset:**
    Obtain the dataset used for training and testing the model. Ensure the dataset is structured according to the project requirements.

4. **Training the Model:**
    Run the training script to train the Random Forest model:
   ```bash
   python train_model.py --dataset_path /path/to/dataset

5. **Testing the Model:**
   Evaluate the model's performance on a test dataset:
   ```bash
   python test_model.py --test_dataset_path /path/to/test_dataset

## Project Structure

```lua
   |-- DeepFake-Voice-Recognition
       |-- data
       |   |-- train
       |   |-- test
       |-- models
       |   |-- random_forest_model.pkl
       |-- utils
       |   |-- feature_extraction.py
       |-- train_model.py
       |-- test_model.py
       |-- requirements.txt
       |-- README.md
```
       
- **Data:** Contains the training and testing datasets.
- **Models:** Stores the trained Random Forest model.
- **Utils:** Includes utility scripts for feature extraction.

## Usage

After training the model, you can use it for detecting deepfake voices in audio recordings. Integrate the trained model into your applications or use the provided scripts for testing.

```python
# Example usage in Python script
from utils.feature_extraction import extract_mfcc_features
from joblib import load

# Load the trained model
model = load("models/random_forest_model.pkl")

# Extract MFCC features from audio
audio_path = "path/to/audio/file.wav"
features = extract_mfcc_features(audio_path)

# Make a prediction
prediction = model.predict([features])

print("Predicted Class:", prediction)
```
