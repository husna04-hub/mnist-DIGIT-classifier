# 🔢 MNIST Digit Classifier — CNN

## Overview
Convolutional Neural Network that recognizes handwritten 
digits (0-9) from the MNIST dataset, achieving 99.17% 
test accuracy in just 10 training epochs.

## Results
| Metric          | Score     |
|-----------------|-----------|
| Test Accuracy   | 99.17% ✅ |
| Target          | 98.00%    |
| Parameters      | 93,322    |
| Training Epochs | 10        |
| Training Time   | ~10 mins  |

## Model Architecture
```
Input (28×28×1)
    ↓
Conv2D(32, 3×3) → ReLU → MaxPooling(2×2)
    ↓
Conv2D(64, 3×3) → ReLU → MaxPooling(2×2)
    ↓
Conv2D(64, 3×3) → ReLU
    ↓
Flatten → Dense(64) → Dropout(0.5) → Dense(10, Softmax)
```

## Key Concepts Demonstrated
- Convolutional layers for spatial feature extraction
- MaxPooling for dimensionality reduction
- Dropout regularization to prevent overfitting
- Softmax output for multi-class classification

## Tech Stack
Python, TensorFlow, Keras, NumPy, Matplotlib

## How to Run
1. Open `mnist_cnn.ipynb` in Google Colab
2. Runtime → Run All (no GPU needed)
3. Training completes in ~10 minutes

## Sample Predictions
Model correctly classified all 10 test samples including
visually ambiguous handwritten digits.
```

---

## requirements.txt
```
tensorflow
numpy
matplotlib
```

---

## Project Structure
```
mnist-digit-classifier/
├── README.md
├── requirements.txt
└── mnist_cnn.ipynb
