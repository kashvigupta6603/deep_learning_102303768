# Fundamentals of Deep Learning – Project Work

## 📌 Overview

As part of the **NVIDIA: Fundamentals of Deep Learning (Coursera)** course, I worked on hands-on deep learning tasks including image classification, neural networks, and transfer learning.

The project helped me understand how deep learning models learn patterns from images and how pretrained models can be reused to improve performance.

---

## 📂 Datasets Used

### 1️⃣ MNIST Dataset

* 28×28 grayscale handwritten digits
* 10 classes (0–9)
* Used to learn basic neural network classification

### 2️⃣ CIFAR-10 Dataset

* 32×32 color images
* 10 object categories (airplane, cat, dog, truck, etc.)
* Used for transfer learning with VGG16

---

## 🧠 Part 1: MNIST Digit Classification

### ✔ What was done

* Loaded MNIST dataset
* Visualized handwritten digits
* Normalized pixel values (0–255 → 0–1)
* Flattened images (28×28 → 784)
* Converted labels to categorical format
* Built a neural network using Dense layers
* Trained and evaluated the model

### ✔ Model Architecture

* Input: 784 pixels
* Dense layer (ReLU)
* Dense layer (ReLU)
* Output layer (Softmax)

### ✔ What I learned

* How neural networks recognize patterns
* Why normalization improves training
* How softmax gives probability outputs
* How accuracy and loss show learning progress

---

## 🧠 Part 2: Understanding Activation Functions

I explored different activation functions and visualized them:

* Sigmoid
* Tanh
* ReLU
* Leaky ReLU
* ELU
* Softmax

This helped me understand how neural networks introduce non-linearity and make complex decisions.

---

## 🧠 Part 3: Transfer Learning with VGG16 (CIFAR-10)

### ✔ What was done

* Loaded CIFAR-10 dataset
* Normalized image values
* Converted labels to categorical format
* Loaded pretrained VGG16 model (ImageNet weights)
* Removed top classification layers
* Froze convolution layers
* Added custom classification layers
* Trained model on CIFAR-10
* Evaluated performance

### ✔ Why use Transfer Learning?

Instead of training a deep network from scratch:

✔ saves training time
✔ uses learned features
✔ improves performance with less data

---

## 📊 Why did accuracy come around ~60%?

This is normal for a basic transfer learning setup.

### Reasons:

**1️⃣ Image Size Limitation**
VGG16 was trained on **224×224 images**, but CIFAR-10 images are only **32×32**.
Important details are lost.

**2️⃣ Frozen Layers**
We froze all convolution layers, so the model could not adapt fully to CIFAR-10 features.

**3️⃣ Very Few Training Epochs**
Training for only ~10 epochs is not enough for better adaptation.

**4️⃣ No Data Augmentation**
Without rotation, flipping, zooming etc., the model sees limited variations.

**5️⃣ CIFAR-10 is harder than MNIST**
MNIST digits are simple.
CIFAR images have complex backgrounds and objects.

👉 Because of these reasons, **60–70% accuracy is expected** in this basic setup.

---

## 📈 How accuracy can be improved

* Resize images to 224×224
* Unfreeze top VGG layers (fine-tuning)
* Train for more epochs
* Use data augmentation
* Use CNN instead of flatten-only layers

---

## 🎯 Key Concepts Learned

✔ Neural Networks
✔ Activation Functions
✔ Image Classification
✔ CNN fundamentals
✔ Transfer Learning
✔ Feature extraction
✔ Model training & evaluation

---

## 🚀 What this course helped me achieve

This course strengthened my foundation in deep learning and helped me understand how AI models learn from images and make predictions.

I gained practical experience in building, training, and evaluating deep learning models for real-world tasks.

---
