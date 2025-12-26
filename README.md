# 🐔 Broiler Disease Detection Using Deep Learning

This project develops a deep learning–based system for detecting broiler diseases from poultry fecal images. The goal is to support early disease diagnosis and improve poultry health monitoring using computer vision techniques.

## 📘 Dataset

The dataset was collected in the **Arusha and Kilimanjaro regions of Tanzania** between September 2020 and February 2021. Images were captured using the **Open Data Kit (ODK) mobile app** on poultry farms.

Original dataset source: **Kilimanjaro Poultry Fecal Images (Kaggle)**

For this study, images were categorized into **three classes**:

1. **Newcastle**
2. **Normal**
3. **Other Abnormal**

All images were resized to **224 × 224** during preprocessing.

## 🧠 Models Used

The project evaluates multiple CNN transfer learning models:

### 🔹 MobileNetV2
- Image size: 224 × 224  
- Epochs: 50  
- Batch size: 8  
- Learning schedule:
  - `patience = 3`
  - `min_lr = 1e-8`
  - `histogram_freq = 1`

**Results**
- Train Accuracy: **99.98%**
- Validation Accuracy: **98.10%**
- Test Accuracy: **98.56%**
- Validation Loss: **0.083**

---

### 🔹 ResNet50
- 3-class classification
- Image size: 224 × 224  
- Epochs: 50  
- Batch size: 8  
- `patience = 3`, `min_lr = 1e-8`

**Results**
- Train Accuracy: **100%**
- Validation Accuracy: **98.60%**
- Test Accuracy: **99.38%**

---

### 🔹 EfficientNetB0
- 3-class classification
- Image size: 224 × 224  
- Epochs: 70  
- Batch size: 8  
- `patience = 3`, `min_lr = 1e-8`

**Model Parameters**
- Total params: **3,634,534**
- Trainable params: **3,595,711**
- Non-trainable params: **38,823**

**Results**
- Train Accuracy: **99.95%**
- Validation Accuracy: **98.36%**
- Test Accuracy: **99.35%**
- Train Loss: **0.0026**
- Validation Loss: **0.06**

---

## 🛠 Tech Stack

- Python
- TensorFlow / Keras
- Jupyter Notebook
- Transfer Learning (CNNs)

## ▶️ How to Run the Notebook

1. Clone the repository:
```bash
git clone https://github.com/your-username/broiler-disease-detection.git
