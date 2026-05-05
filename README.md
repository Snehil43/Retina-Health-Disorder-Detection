# Retina Health Disorder Detection

This project uses a MobileNetV2-based deep learning model to classify retina images into:
- Healthy
- Diseased

---

## 🚀 Workflow

### 1. Dataset Preparation
- Download retina dataset (APTOS / EyePACS)
- Create two folders:
  - `Healthy`
  - `Diseased`
- Convert labels:
  - 0 → Healthy
  - 1–4 → Diseased

---

### 2. Data Preprocessing
- Resize all images to **224 × 224**
- Normalize pixel values to **[0,1]**
- Split dataset into:
  - **80% Training**
  - **20% Testing**

---

### 3. Model Building
- Used **MobileNetV2 (pre-trained on ImageNet)**
- Removed top layer
- Added:
  - GlobalAveragePooling
  - Dense layer (Sigmoid activation)

---

### 4. Model Training
- Loss function: Binary Crossentropy
- Optimizer: Adam
- Epochs: 3
- Validation data used during training

---

### 5. Evaluation
- Accuracy
- Precision
- Recall
- Confusion Matrix

---

### 6. Visualization
- Plotted:
  - Training accuracy
  - Validation accuracy

---

### 7. Explainability (Grad-CAM)
- Used Grad-CAM to visualize model attention
- Generated heatmaps for:
  - Healthy images
  - Diseased images

---

## 📊 Results
- Achieved ~90–91% validation accuracy
- Balanced performance across both classes

---

## 🔮 Future Improvements
- Use larger dataset
- Train for more epochs
- Fine-tune deeper layers
