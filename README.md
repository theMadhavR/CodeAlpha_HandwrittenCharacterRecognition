# Handwritten Character Recognition using CNN

A deep learning project that uses a Convolutional Neural Network (CNN) to recognize handwritten characters from the EMNIST Balanced dataset. The model is built using TensorFlow and Keras and is capable of classifying digits and letters with high accuracy.

---

## Features

* Handwritten character recognition using CNN
* Trained on the EMNIST Balanced dataset
* Image preprocessing and normalization
* Batch Normalization and Dropout for improved performance
* Model evaluation using confusion matrix
* Visualization of sample images and training metrics

---

## Tech Stack

* Python
* TensorFlow
* TensorFlow Datasets (TFDS)
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Project Structure

```text
.
├── notebook.ipynb          # Complete model training and evaluation
└── README.md               # Project documentation
```

---

## Dataset

This project uses the **EMNIST Balanced** dataset provided by TensorFlow Datasets.

* **Training samples:** 112,800
* **Test samples:** 18,800
* **Image size:** 28 × 28 grayscale
* **Classes:** 47 handwritten characters(digits(0-9), some merged uppercase and lowercase alphabets, remaining uppercase alphabets, remaining lowercase alphabets)

Dataset can be loaded directly through:

```python
import tensorflow_datasets as tfds

dataset = tfds.load('emnist/balanced', split=['train', 'test'], as_supervised=True)
```

---

## Model Architecture

The CNN consists of:

* 3 Convolutional layers
* Batch Normalization
* Max Pooling layers
* Dropout layers for regularization
* Fully connected Dense layers
* Softmax output layer

### Architecture Overview

```text
Input (28×28×1)
      ↓
Conv2D (32) + BatchNorm
      ↓
MaxPooling + Dropout
      ↓
Conv2D (64) + BatchNorm
      ↓
MaxPooling + Dropout
      ↓
Conv2D (128) + BatchNorm
      ↓
MaxPooling + Dropout
      ↓
Flatten
      ↓
Dense (512) + Dropout
      ↓
Dense (256) + Dropout
      ↓
Output Layer (47 classes)
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

Install dependencies:

```bash
pip install "tensorflow>=2.15.0" "tensorflow-datasets>=4.9.0" "numpy>=1.24.0" "matplotlib>=3.8.0" "seaborn>=0.13.0" "scikit-learn>=1.4.0" "jupyter>=1.0.0" "ipykernel>=6.0.0"
```

---

## Running the Project

Open the Jupyter notebook:

```bash
jupyter notebook notebook.ipynb
```

Run all cells to:

1. Load the dataset
2. Preprocess the images
3. Train the CNN model
4. Evaluate performance
5. Visualize predictions and metrics

---

## Evaluation Metrics

The model performance is analyzed using:

* Accuracy
* Loss curves
* Confusion Matrix
* Visualization of predictions

---

## Sample Workflow

```text
Dataset
   ↓
Preprocessing
   ↓
CNN Training
   ↓
Model Evaluation
   ↓
Prediction
```

---

## Future Improvements

* Real-time handwritten character recognition
* Web application deployment
* Model optimization for faster inference
* Support for custom handwritten datasets
* Export trained model for mobile and edge devices

---
