# CIFAR-10 Image Classification using VGG16 (Transfer Learning)

## 📌 Project Overview

This project classifies images from the CIFAR-10 dataset using a pre-trained VGG16 model.
Instead of training from scratch, we reuse learned features from ImageNet and train only the final layers.

This makes training faster and improves accuracy.

---

## 📂 Dataset

We use the CIFAR-10 dataset.

It contains:

* 60,000 color images
* Image size: 32 × 32
* 10 classes:
  airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

The dataset is loaded directly using TensorFlow/Keras.

---

## ⚙️ Steps Performed

### 1️⃣ Load Dataset

CIFAR-10 data is loaded and split into training and testing sets.

### 2️⃣ Normalize Images

Pixel values are scaled from **0–255 → 0–1**
This helps the model train faster and more accurately.

### 3️⃣ Convert Labels

Labels are converted into one-hot encoded format for multi-class classification.

### 4️⃣ Load Pretrained VGG16

We load the VGG16 model with:

* pretrained ImageNet weights
* top layers removed (`include_top=False`)

This allows us to use VGG16 as a feature extractor.

### 5️⃣ Freeze Base Layers

All convolution layers are frozen so their learned features remain unchanged.

### 6️⃣ Add Custom Layers

We add:

* Flatten layer
* Dense layer (ReLU)
* Dropout layer (prevents overfitting)
* Output layer (Softmax with 10 classes)

### 7️⃣ Compile Model

We use:

* Optimizer: Adam
* Loss: Categorical Crossentropy
* Metric: Accuracy

### 8️⃣ Train Model

The model is trained on CIFAR-10 images.

### 9️⃣ Evaluate Performance

The trained model is tested on unseen images to measure accuracy.

---

## 🧠 Why Transfer Learning?

Training deep networks from scratch requires huge data and time.

Transfer learning:
✔ uses pretrained knowledge
✔ trains faster
✔ improves accuracy
✔ works well with small datasets

---

## 📊 Expected Results

After training for a few epochs, accuracy typically reaches:

👉 **70% – 85%**

This can be improved with more training and data augmentation.

---

## 🚀 How to Run

1. Install TensorFlow
2. Open the notebook
3. Run all cells in order
4. Wait for training to complete
5. Check test accuracy

---

## ✅ Key Concepts Used

* Deep Learning
* Transfer Learning
* Convolutional Neural Networks (CNN)
* VGG16 Architecture
* Image Classification

---

## 📌 Notes

* Ignore memory warnings if they appear.
* Training may take time on CPU.
* Using GPU will speed up training.

---

## 🎯 Future Improvements

* Add data augmentation
* Fine-tune top VGG layers
* Train longer for better accuracy
* Deploy as a web app

---
