# 🐾 Animal Image Classification with CNNs and Ensemble Learning

This project implements an end-to-end pipeline for classifying images of animals using Convolutional Neural Networks (CNNs) and ensemble learning techniques. It is built using TensorFlow/Keras and explores different model architectures, data preprocessing techniques, and model evaluation metrics.

## 📁 Dataset

The dataset is organized into three folders:
Animals_DataSet/
  ├── Training_Set/
  ├── Validation_Set/
  └── Test_Set/


Each subfolder contains six class directories:

- `butterfly/`
- `cat/`
- `cow/`
- `elephant/`
- `sheep/`
- `squirrel/`

Images are preprocessed by resizing to 32x32 pixels and normalized to the `[0, 1]` range.

---

## 🧠 Models

Three different CNN architectures are trained and evaluated:

### Model 1: Baseline CNN
- 4 convolutional layers with increasing filters.
- Batch normalization, max pooling, and dropout.
- Global Average Pooling for dimensionality reduction.

### Model 2: Activation & Regularization Optimized
- Uses LeakyReLU activations and L2 regularization.
- Higher number of filters.
- Optimized using the Adam optimizer.

### Model 3: Depth & Stride Optimized
- Deeper architecture with more layers.
- Stronger dropout and regularization.
- Trained with higher learning rate.

---

## ⚙️ Features

- ✅ Image loading and preprocessing
- ✅ One-hot encoding of labels
- ✅ Data augmentation (`ImageDataGenerator`)
- ✅ Training and validation with metrics tracking
- ✅ Visualization of training progress (loss/accuracy curves)
- ✅ Confusion matrix, ROC and PR curve generation
- ✅ Ensemble voting for final predictions
- ✅ Prediction comparison saved to CSV

---

## 📊 Evaluation

- Models are compared using accuracy, confusion matrices, ROC-AUC, and Precision-Recall metrics.
- Ensemble voting improves overall classification performance.
- Performance plots (validation accuracy/loss, ROC, PR) are automatically generated.

---

## 🔧 How to Run

1. Clone the repository and set up your environment:
   ```bash
   pip install -r requirements.txt
