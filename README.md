# Audio Deepfake Detection System (CNN-Based)

## Overview

This project focuses on detecting deepfake audio using Mel Spectrograms and deep learning techniques. The work evolved through multiple model explorations, starting with traditional machine learning approaches and progressing toward deep learning to better capture complex audio patterns.

Initially, various models such as Random Forest and XGBoost were implemented. Later, to better capture the complexity of audio signals, a Convolutional Neural Network (CNN) was adopted as the final model.

---

## Project Evolution

* Initial implementation of traditional machine learning models (Random Forest, XGBoost)
* Integration of a Support Vector Machine (SVM) model as an individual contribution
* Identification of limitations of traditional models in capturing complex audio patterns
* Transition to CNN-based architecture for improved feature learning

The final results indicate that CNN performs best for this task.

---

## Contribution

This was a group project in which multiple models were explored collaboratively.

* Primary contribution: Implementation of the SVM-based audio detection model
* Participation in preprocessing, experimentation, and evaluation
* Contribution to comparative analysis across models

---

## Models and Performance

* Random Forest: ~94% accuracy
* XGBoost: ~98% accuracy
* SVM: Baseline model for comparison
* CNN (final model): ~98% accuracy with improved reliability

---

## Dataset

* Dataset: ASVspoof 2019 (Logical Access)
* Contains real and spoof (deepfake) audio samples
* Audio clips standardized to 3 seconds
* Converted into Mel Spectrograms for model input
* Dataset was highly imbalanced (more spoof than real samples)

---

## Challenges

* Severe class imbalance leading to biased predictions
* Initial CNN performance around 70% accuracy
* Accuracy was misleading due to imbalance
* Poor performance on the minority (real) class

---

## Improvements

* Applied class weights to address imbalance
* Performed data augmentation:

  * Noise addition
  * Pitch shifting
  * Time stretching
* Added additional features:

  * Delta features
  * Min and max values
* Normalized Mel Spectrogram inputs
* Used early stopping to prevent overfitting
* Focused on recall as a key evaluation metric

---

## Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

---

## Key Observations

* Traditional machine learning models showed high accuracy but were biased toward the majority class
* Accuracy alone was not a reliable evaluation metric in imbalanced settings
* CNN initially underperformed due to preprocessing and imbalance issues
* After applying corrective strategies, CNN performance improved significantly
* CNN demonstrated better capability in capturing complex audio patterns

---

## Techniques Used

* Audio standardization (3-second clips)
* Mel Spectrogram feature extraction
* Data augmentation techniques
* Class imbalance handling using class weights
* Feature engineering
* Early stopping for regularization

---

## Project Structure

audio-deepfake-detection-v2/

├── svm_model/            (individual contribution)
├── cnn_model/            (final model)
├── random_forest/
├── xgboost/
├── demo_video/
├── dataset_info/
└── README.md

---

## Evaluation Outputs

* Confusion Matrix
* Classification Report
* Accuracy and loss curves

---

## Key Learning

Handling class imbalance and selecting appropriate evaluation metrics (particularly recall over accuracy) were critical in achieving reliable performance. Deep learning models such as CNNs are more effective in capturing complex audio patterns compared to traditional machine learning approaches.

---

## Tech Stack

* Python
* TensorFlow / Keras
* Librosa
* Scikit-learn

---

## Author

Harshini Hasalkar
Second Year, Computer Engineering
Dr. D. Y. Patil Institute of Technology

---

## Note

This repository includes earlier experimental files and a ZIP archive used during development.


