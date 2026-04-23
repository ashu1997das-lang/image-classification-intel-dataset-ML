# Image Classification using MobileNetV2

🚀 End-to-end image classification project using transfer learning, achieving **84% accuracy on unseen test data**.

---

## 🔍 Quick Highlights
- ✅ Transfer Learning (MobileNetV2)
- ✅ Data Augmentation to reduce overfitting
- ✅ Fine-tuning for better generalization
- ✅ 84% Test Accuracy
- ✅ Real-time prediction on new images

---

## ▶️ How to Run

1. Open the notebook in Google Colab  
2. Upload your dataset (train/val/test structure)  
3. Run all cells step-by-step  
4. Train the model  
5. Evaluate on test data  
6. Upload an image to test prediction

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

## 📸 Sample Output

![Model Output](ml_training_prediction_sample.png)

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
