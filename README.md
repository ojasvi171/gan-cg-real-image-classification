# 🧠 GAN vs CG vs Real Image Classification (Advanced AI/ML Project)

## 📌 Overview

This project focuses on **multi-class image forensics**, aiming to classify images into:

* 🟢 Real (Photographic Images)
* 🔵 Computer-Generated (CG Images)
* 🔴 GAN-Generated Images

With the increasing use of **AI-generated content and deepfakes**, detecting synthetic media has become critical for **digital forensics, cybersecurity, and misinformation control**.

---

## 🎯 Problem Statement

Unlike traditional approaches that perform **binary classification (Real vs Fake)**, this project tackles a more challenging task:

➡️ **Three-class classification:** GAN vs CG vs Real
➡️ Handles **high similarity between CG and Real images**
➡️ Detects **subtle noise, texture, and rendering artifacts**

---

## 🧠 Methodology

### 🔹 Two-Stream Architecture (Core Model)

The base system uses a **two-stream deep learning approach**:

1. **Feature Stream – EfficientNetB0**

   * Transfer learning with ImageNet weights
   * Captures high-level semantic features

2. **Artifact Stream – Custom CNN**

   * Detects low-level noise and pixel inconsistencies
   * Helps identify GAN artifacts and lack of camera noise in CG images

➡️ Outputs are fused for final classification.

---

### 🔹 Improved Model (ResNet50 Enhancement)

To further improve performance, an additional model using **ResNet50** was implemented:

* Deep residual architecture for better feature learning
* Improved convergence and generalization
* Helped boost classification accuracy significantly

➡️ This model was used for:

* performance comparison
* improving robustness
* validating architectural choices

---

### 🔹 Key Techniques Used

* Transfer Learning (EfficientNetB0, ResNet50)
* Data Augmentation
* Class Imbalance Handling (Focal Loss + Class Weights)
* Fine-Tuning (layer unfreezing)
* Ensemble Learning (multi-phase training)
* Grad-CAM (Explainable AI)

---

## 📂 Dataset

* Total Images: ~12,000
* Classes: GAN, CG, Real
* Split:

  * Training: 60%
  * Validation: 20%
  * Testing: 20%

⚠️ Dataset not included due to size constraints.

---

## ⚙️ Tech Stack

* Python
* TensorFlow / Keras
* OpenCV
* NumPy, Pandas
* Matplotlib

---

## 📊 Results & Insights

* Significant improvement in accuracy after ResNet50 experimentation
* GAN images are easiest to detect
* CG images remain the most challenging due to realism
* Two-stream + deep backbone improves classification performance
* Model shows robustness under compression and transformations

---

## 🔍 Explainability (Grad-CAM)

Grad-CAM is used to visualize **important regions influencing predictions**, making the model more interpretable and trustworthy.

---

## 📁 Project Structure

```id="n3v7nq"
├── gancgreal.ipynb               # Base model (EfficientNet), Fine-tuning, Balanced training
├── gancgrealpart2.ipynb          # Improvements
├── gancgrealpart3.ipynb          # Improvements
├── RESNET50 MODEL.ipynb          # Improved model (higher accuracy)
├── gradcamadded.ipynb            # Grad-CAM visualization
├── README.md
```

---

## 🚀 Key Features

* Multi-class classification (GAN vs CG vs Real)
* Two-stream CNN architecture
* ResNet50-based performance improvement
* Handles class imbalance effectively
* Explainable AI using Grad-CAM
* Designed for real-world forensic applications

---

## 📚 References

1. M.P. Gangan et al., *Multi-Colorspace Fused EfficientNet*, 2021
2. K.B. Meena & V. Tyagi, *Two-stream CNN for CG Detection*, 2020

---

## 🔮 Future Work

* Deploy as a web app (Streamlit / Flask)
* Real-time image classification API


---

## 👩‍💻 Author

**Ojasvi Mishra**
B.Tech CSE
Jaypee University of Engineering & Technology

---

## ⭐ Note

This project demonstrates advanced concepts in **deep learning, image forensics, and explainable AI**, combining multiple architectures and optimization strategies for improved performance.

