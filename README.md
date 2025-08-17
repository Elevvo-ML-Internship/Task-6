# 🎶 Music Genre Classification (ML & Audio Features)

## 📌 Overview

This project implements a **music genre classification system** using machine learning models trained on extracted audio features.  
The dataset used is the classic **GTZAN dataset** containing 10 genres.

We extract features like **MFCCs, spectral contrast, chroma features, tonnetz, tempo**, and more using **Librosa**.  
Then we train and evaluate multiple ML models: **Random Forest, Decision Tree, Logistic Regression, and XGBoost**.

---
## 📂 Dataset

- Source: **GTZAN Genre Dataset** (`genres_original/`)
- Genres: `blues, classical, country, disco, hiphop, jazz, metal, pop, reggae, rock`
- Total files: **1000 audio tracks (30s each)**
- Training/Test split: **80/20**
- [Download from Kaggle](https://www.kaggle.com/datasets/carlthome/gtzan-genre-collection)
- After downloading:
	1. Extract the dataset.
	2. Rename the folder from `genres` to `genres_original`.
	3. Place it inside the project root folder

⚠️ One file was skipped due to format error:

```
Skipping genres_original\jazz\jazz.00054.wav (Format not recognised)
```

✅ Extracted features from **999 files**  
✅ Feature count: **53**

---

## 🛠️ Models & Results

### 📊 RandomForest

**Accuracy:** `0.8000` ✅ _(Best Model)_

```
precision    recall  f1-score   support

blues       0.83      0.71      0.77        21
classical   0.71      1.00      0.83        12
country     0.77      0.71      0.74        24
disco       1.00      0.82      0.90        22
hiphop      0.76      0.87      0.81        15
jazz        0.92      0.89      0.91        27
metal       0.86      1.00      0.92        18
pop         0.81      0.89      0.85        19
reggae      0.81      0.77      0.79        22
rock        0.47      0.45      0.46        20

Accuracy                        0.80       200
```

---

### 📊 DecisionTree

**Accuracy:** `0.6350`

---

### 📊 LogisticRegression

**Accuracy:** `0.7350`

---

### 📊 XGBoost

**Accuracy:** `0.7800`

---

## 🏆 Best Model

- **RandomForest** achieved the highest performance with **80% accuracy**.
- It balanced precision and recall across most genres, though **rock** remained the most challenging class to predict.

---

## 🎧 Test Predictions

```
test\classical.00005.wav → classical
test\pop.00000.wav       → pop
test\rock.00001.wav      → rock
```

---

## 🚀 Tech Stack

- **Python**
- **Librosa** (audio feature extraction)
- **Scikit-learn** (ML models)
- **XGBoost** (boosted trees)
- **Pandas, Numpy, Matplotlib**
