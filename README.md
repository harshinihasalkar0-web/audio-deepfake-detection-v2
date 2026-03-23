# audio-deepfake-detection-v2
CNN-based audio deepfake detection using Mel spectrograms
# Audio Deepfake Detection using CNN

## Overview
This project focuses on detecting deepfake audio using Mel Spectrograms and deep learning (CNN). It also includes a comparison with traditional machine learning models.

## Dataset
- Dataset used: ASVspoof 2019 (Logical Access)
- Contains real and spoof (deepfake) audio samples
- Audio clips standardized to 3 seconds
- Converted to Mel Spectrograms for model input
- Dataset was highly imbalanced (more spoof than real samples)

---

## Models & Performance
- Random Forest: 94% accuracy
- XGBoost: 98% accuracy
- CNN (final model): ~98% accuracy
- ## Challenges Faced
- Severe class imbalance caused biased predictions
- CNN initially performed around 70% accuracy
- Accuracy was misleading due to imbalance
- Model struggled with real-class predictions

  ## Improvements & Fixes
- Applied class weights to balance classes
- Used data augmentation (noise, pitch shift, time stretch)
- Added extra features (delta, min, max)
- Normalized Mel spectrograms
- Used Early Stopping to reduce overfitting
- Focused on recall instead of only accuracy

## Evaluation Metrics
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix
---

## Key Observations
- Traditional ML models showed high accuracy even with imbalanced data, but performance was biased toward the majority class.
- Accuracy alone was not a reliable metric in this case.
- The CNN model initially achieved around 70% accuracy due to class imbalance and lack of normalization.
- After addressing preprocessing issues and balancing strategies, the CNN performance improved significantly.

---

## Techniques Used
- Audio standardization (3-second clips)
- Mel Spectrogram feature extraction
- Data augmentation (noise, pitch shift, time stretch)
- Class imbalance handling using class weights
- Feature engineering (delta features, min/max values)
- Early stopping to prevent overfitting

---

## Evaluation
- Confusion Matrix
- Classification Report (precision, recall, F1-score)
- Accuracy and loss curves

---

## Tech Stack
- Python
- TensorFlow / Keras
- Librosa
- Scikit-learn
