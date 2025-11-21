# 🤟 Sign Language ABC Classification  

## Deep Learning Project — WBS Coding School  
This project uses **Convolutional Neural Networks (CNNs)** and **transfer learning** to classify hand signs for the letters **A**, **B**, and **C** in German Sign Language (DGS).  
Using EfficientNet and careful data preparation, the final model reached **91.92% accuracy** on the hidden competition test set.

---

## 🎯 Objective  
The goal of this project is to train a model that can correctly identify the letters **A**, **B**, and **C** from images of hand signs.

> 🧠 *Teaching a neural network to learn its ABCs — one hand sign at a time.*

---

## 🖼️ Dataset Preview  

<img src="images/dataset-card-1.png" alt="Dataset preview of signs A, B, C" width="600"/>

---

## 📂 Repository Contents  
- 📓 **notebooks/B2_TheWinnerModel.ipynb** — ⭐ **final winning notebook (EfficientNetB2)**  
- 📓 notebooks/ — other experiment notebooks:
  - CNN baseline  
  - Image augmentation  
  - L2 regularisation  
  - Transfer learning experiments (B0, B1, B2)  
- 🤖 **models/sign_efficientnetB2_clean_competition.keras** — ⭐ **final winning model**  
- 📂 images/ — project visuals (including dataset-card-1.png)  
- 📄 README.md — project documentation  
- 📄 .gitignore  

---

## 🧑‍💻 Approach  

### 1️⃣ Data Collection  
- Collected custom hand-sign photos for **A**, **B**, and **C**  
- Captured images with varied:
  - lighting  
  - backgrounds  
  - camera angles  
  - distances  

### 2️⃣ Data Preparation  
- Organised raw images into class folders  
- Split into **train** and **validation** sets  
- Applied **real-time image augmentation** using Keras:
  - RandomFlip  
  - RandomRotation  
  - RandomZoom  
  - RandomContrast  

### 3️⃣ Model Development  
- Started with baseline CNN models  
- Introduced:
  - **Dropout**  
  - **L2 regularisation**  
  - Batch Normalisation  
- Performed transfer learning with:
  - **EfficientNetB0**  
  - **EfficientNetB1**  
  - **EfficientNetB2** (winner)

### 4️⃣ Final Model — EfficientNetB2  
- Two-stage training:
  1. Train classifier head  
  2. Unfreeze backbone for fine-tuning  
- Used callbacks:
  - ReduceLROnPlateau  
  - EarlyStopping  
  - ModelCheckpoint  
- Achieved competition-winning accuracy.

---

## 🎧 Results  

### 🏆 Final Performance  
- **Competition accuracy:** 91.92%  
- **Validation accuracy:** 100%  
- **Best model:** `sign_efficientnetB2_clean_competition.keras`

### Classification Report (Validation Set)

| Class | Precision | Recall | F1-Score |
|------|-----------|--------|----------|
| A | 1.00 | 1.00 | 1.00 |
| B | 1.00 | 1.00 | 1.00 |
| C | 1.00 | 1.00 | 1.00 |

> 🚀 The EfficientNetB2 model generalised best and became the winner of the internal competition.

---

## 🛠 Tools Used  
1. **Python** — TensorFlow, Keras, NumPy  
2. **EfficientNetB2** — transfer learning backbone  
3. **Matplotlib** — visualisations  
4. **Jupyter Notebooks** — experimentation  

---

## 🎓 Key Learnings  
1. Image quality & dataset diversity strongly influence performance  
2. Transfer learning significantly boosts model accuracy  
3. Data augmentation prevents overfitting  
4. Fine-tuning only the top layers is not enough — full-network fine-tuning matters  
5. Proper callbacks stabilise and optimise training  

---

## 💡 Final Summary  
✅ Built a complete sign-language image classifier  
✅ Achieved **91.92%** accuracy on the test set  
✅ EfficientNetB2 proved the best feature extractor  
✅ Demonstrated full deep-learning workflow:  
*data → augmentation → CNN → transfer learning → fine-tuning → evaluation*

> 🤟 *A small project with a simple goal: help a model learn its ABCs.*  
