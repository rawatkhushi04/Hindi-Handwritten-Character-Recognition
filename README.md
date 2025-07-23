# 📝 Devanagari Handwritten Character Recognition using CNN

This project focuses on building a Convolutional Neural Network (CNN) to classify handwritten Devanagari characters. 
It uses the [Devanagari Handwritten Character Dataset](https://www.kaggle.com/datasets/medahmedkrichen/devanagari-handwritten-character-datase/data)and leverages deep learning techniques
to identify characters from images.

---

## 📌 Project Overview

The Devanagari script is used for over 120 languages including Hindi, Sanskrit, Marathi, and Nepali. Automatic recognition of handwritten characters can assist in digitizing documents, educational applications, and optical character recognition (OCR).

This project uses a CNN model built with TensorFlow and Keras to recognize 46 different Devanagari characters.

---
## 📂 Dataset

- **Source**: [Devanagari Handwritten Character Dataset](https://www.kaggle.com/datasets/medahmedkrichen/devanagari-handwritten-character-datase)
- This is an image database of Handwritten Devanagari characters. There are 46 classes of characters with 2000 examples each. The dataset is split into a training set(85%) and a testing set(15%) from the UCI machine learning Repository.
- **Format**: Images grouped in folders per character
- **Size**: Each image is resized to **32x32 pixels**

---

## 🧠 Model Architecture

- **Type**: CNN using Keras Sequential API
- **Input Shape**: `(32, 32, 1)` (grayscale) or `(32, 32, 3)` (color)
- **Layers**:
  - Rescaling Layer
  - Convolutional Layers (ReLU activation)
  - Batch Normalization
  - MaxPooling Layers
  - Flatten Layer
  - Dense Layers (Fully Connected)
  - Output Layer (Softmax Activation with 46 units)

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- Matplotlib
- Google Colab / Jupyter Notebook

---

## 🚀 How to Run

1. Clone this repository or upload the notebook to [Google Colab](https://colab.research.google.com/).
2. Download and extract the Devanagari dataset.
3. Load the dataset using `ImageDataGenerator` or manual preprocessing.
4. Train the model using:

   ```python
   model.fit(training_dataset, validation_data=testing_dataset, epochs=10)
