# CIFAR-10 CNN Image Classification

A Convolutional Neural Network (CNN) project built with **Python, TensorFlow, Keras, NumPy, and Matplotlib** to classify images from the CIFAR-10 dataset into **cats and dogs**.

## 📌 Project Overview

This project uses the **CIFAR-10 dataset** and focuses on binary image classification.

The original CIFAR-10 dataset contains 10 different image classes. This project filters the dataset to use only:

* **Cat** → CIFAR-10 label `3`
* **Dog** → CIFAR-10 label `5`

The CNN learns visual patterns from the images and predicts whether a given image is a cat or a dog.

## 🧠 How It Works

The project follows these steps:

1. **Load CIFAR-10**

   * Loads the training and testing images using TensorFlow/Keras.

2. **Filter the dataset**

   * Keeps only images labeled as cats (`3`) and dogs (`5`).

3. **Convert labels**

   * Cat → `0`
   * Dog → `1`

4. **Normalize images**

   * Pixel values are divided by `255.0`.
   * This converts pixel values from `0–255` to `0–1`.

5. **Build the CNN**

   * Convolutional layers extract visual features.
   * MaxPooling reduces the spatial size.
   * Flatten converts the extracted features into a vector.
   * Dense layers perform the final classification.

6. **Train the model**

   * Optimizer: Adam
   * Loss: Binary Crossentropy
   * Epochs: `10`
   * Batch size: `64`

7. **Evaluate the model**

   * The trained model is evaluated on the test dataset.
   * Test accuracy is displayed.

8. **Make a prediction**

   * A random test image is selected.
   * The model predicts whether it is a cat or dog.
   * The actual label is also displayed.

## 🏗️ Model Architecture

```text
Input Image
32 × 32 × 3
      ↓
Conv2D
32 Filters
      ↓
MaxPooling
      ↓
Conv2D
64 Filters
      ↓
MaxPooling
      ↓
Flatten
      ↓
Dense
128 Neurons
      ↓
Dense
1 Neuron
      ↓
Sigmoid
      ↓
Cat / Dog
```

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Convolutional Neural Networks (CNN)

## 📂 Project Structure

```text
cifar10-cnn/
│
├── cifar10_cnn.py
├── requirements.txt
└── README.md
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/AbdullahKamal9/cifar10-cnn.git
```

Move into the project directory:

```bash
cd cifar10-cnn
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## ▶️ Run the Project

Run the Python file:

```bash
python cifar10_cnn.py
```

The CIFAR-10 dataset will be automatically downloaded by Keras the first time the program runs.

The model will then train for 10 epochs and evaluate its performance on the test dataset.

## 📊 Classification

The project converts the original CIFAR-10 labels into binary labels:

| Original CIFAR-10 Label | Class | New Label |
| ----------------------- | ----- | --------- |
| `3`                     | Cat   | `0`       |
| `5`                     | Dog   | `1`       |

The model uses a **Sigmoid activation function** in the final layer because this is a binary classification problem.

## 🎯 Prediction

After training, the program randomly selects an image from the test set and makes a prediction:

```text
It is a dog
Actual label: Dog
```

or:

```text
It is a cat
Actual label: Cat
```

The selected image is also displayed using Matplotlib.

## 📚 What I Learned

This project demonstrates:

* Loading datasets with Keras
* Image preprocessing
* Image normalization
* Binary classification
* Convolutional Neural Networks
* Convolution layers
* MaxPooling layers
* Flattening feature maps
* Dense layers
* Sigmoid activation
* Binary cross-entropy loss
* Model training and evaluation
* Making predictions with a trained CNN

## ⚠️ Note

This is a basic CNN implementation for learning purposes. The CIFAR-10 images are only **32×32 pixels**, so the model is relatively small and the classification performance is limited compared with modern computer vision models.

## 👨‍💻 Author

**Abdullah Kamal**

GitHub: https://github.com/AbdullahKamal9
