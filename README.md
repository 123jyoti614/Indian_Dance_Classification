# 🩰 Indian Classical Dance Form Classification

This deep learning project uses **Transfer Learning with MobileNetV2** to classify images of **8 Indian classical dance forms** from photos. It was developed as part of a computer vision assignment to promote and recognize the rich diversity of Indian dance styles.

---

## 📚 Classes of Dance Forms

The model classifies images into one of the following categories:

- **Bharatanatyam**
- **Kathak**
- **Kathakali**
- **Kuchipudi**
- **Manipuri**
- **Mohiniyattam**
- **Odissi**
- **Sattriya**

---

## 📁 Dataset Overview

- **Train set**: 364 labeled images (8 classes)
- **Test set**: 156 unlabeled images
- Format: JPEG images with corresponding `train.csv` and `test.csv`

> *Note: Dataset not included here due to size. Please upload it separately to your Google Colab environment.*

---

## ✅ Model Details

- **Architecture**: MobileNetV2 (pretrained on ImageNet)
- **Input Size**: 224x224
- **Preprocessing**: Normalization using `preprocess_input` from MobileNetV2
- **Data Augmentation**: Rotation, flipping, zoom, etc.
- **Fine-tuning**: Top 30 layers of MobileNetV2 unfrozen and retrained
- **Final Validation Accuracy**: ~68%
- **Best Performing Class**: Kathakali (F1-score: 0.95)

---

## 🔎 Evaluation Results

| Metric       | Score |
|--------------|-------|
| Accuracy     | 68%   |
| Macro F1     | 0.69  |
| Precision    | 0.72  |
| Recall       | 0.68  |

- Weak classes (e.g., Kuchipudi, Bharatanatyam) had fewer samples and more confusion.
- Confusion matrix and classification report were used to diagnose model performance.

---

## 🔧 How to Run

> Use Google Colab for training and inference.

1. Upload your dataset ZIP (with `train`, `test`, `train.csv`, `test.csv`) to Colab
2. Run the notebook:
   - `notebook/Indian_Dance_Classifier.ipynb`
3. Generate predictions
4. Submit `submission_mobilenetv2.csv` as output

---

## 📦 Files in This Repo

| File / Folder                    | Description                          |
|----------------------------------|--------------------------------------|
| `notebook/Indian_Dance_Classifier.ipynb` | Main training & inference notebook |
| `submission/submission_mobilenetv2.csv` | Predicted dance classes for test set |
| `requirements.txt`              | Python libraries used                |
| `README.md`                     | Project documentation                |

---

## 🚀 Future Improvements

- Use larger datasets with balanced class samples
- Try EfficientNetB0 or ResNet50 for improved generalization
- Implement Grad-CAM visualizations for interpretability

---
