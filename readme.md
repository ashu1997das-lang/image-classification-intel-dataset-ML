# Image Classification using MobileNetV2

## 📌 Overview
This project builds an end-to-end image classification pipeline to classify natural scene images into six categories using transfer learning.

---

## 🗂️ Classes
- Building  
- Forest  
- Glacier  
- Sea  
- Mountain  
- Street  

---

## 📊 Dataset
- ~300 images  
- Labeled using Label Studio  
- Organized into:
  - Train set  
  - Validation set  
  - Test set  

---

## ⚙️ Methodology

### 1. Data Preparation
- Cleaned labels from CSV  
- Organized images into folder structure  
- Created stratified train/validation/test splits  

---

### 2. Model Architecture
- Pretrained **MobileNetV2** (ImageNet weights)  
- Removed top layers  
- Added:
  - GlobalAveragePooling  
  - Dense (128, ReLU)  
  - Output layer (Softmax, 6 classes)  

---

### 3. Training
- Initial baseline training  
- Observed overfitting (high train accuracy vs lower validation accuracy)

---

### 4. Improvement
- Applied **data augmentation**:
  - Rotation  
  - Zoom  
  - Horizontal flip  
- Helped improve generalization  

---

### 5. Fine-Tuning
- Unfroze last few layers of base model  
- Used low learning rate  
- Improved model adaptability to dataset  

---

## 📈 Results

- Training Accuracy: ~80%  
- Validation Accuracy: ~82–84%  
- **Test Accuracy: ~84%**

---

## 🔍 Evaluation
- Evaluated model on unseen test dataset  
- Generated predictions for new images  

---

## 🚀 Demo
The model can take an input image and predict its class label.

---

## 🛠️ Tech Stack
- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  
- Google Colab  

---

## 📁 Project Structure

image-classification-intel/
│
├── dataset/
│ ├── train/
│ ├── val/
│ └── test/
│
├── training_intel.ipynb
├── requirements.txt
├── README.md

---

## 🧠 Key Learnings
- Handling overfitting in small datasets  
- Importance of data augmentation  
- Transfer learning for efficient model building  
- Fine-tuning pretrained models  

---


## 📥 Dataset

The full dataset is not included due to size limitations.

This project uses the Intel Image Classification dataset, annotated using Label Studio.

To replicate:
1. Download the Intel Image dataset
2. Use the provided structure (train/val/test)
3. Apply the same preprocessing steps

---


## 📌 Conclusion
This project demonstrates a complete machine learning workflow, from data preparation to model evaluation, using transfer learning to achieve strong performance on a small dataset.

---