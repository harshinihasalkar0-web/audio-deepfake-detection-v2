# audio-deepfake-detection-v2
CNN-based audio deepfake detection using Mel spectrograms
# Audio Deepfake Detection using CNN

## Overview
This project focuses on detecting deepfake audio using Mel Spectrograms and deep learning (CNN). It also includes a comparison with traditional machine learning models.

---

## Models & Performance
- Random Forest: 94% accuracy
- XGBoost: 98% accuracy
- CNN (final model): ~98% accuracy

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
