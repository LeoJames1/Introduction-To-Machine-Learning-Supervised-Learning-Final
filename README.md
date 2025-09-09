# Spotify Song Popularity Prediction Project  

This project explores how supervised machine learning can be applied to predict the popularity of Spotify tracks based on their audio and metadata features. It was developed as the final project for *Introduction to Machine Learning: Supervised Learning*.  

---

## 📌 Project Overview  
- **Goal:** Predict Spotify track popularity (0–100) using supervised machine learning.  
- **Approach:** Build, compare, and interpret different regression models.  
- **Outcome:** Demonstrated that tree-based ensemble methods significantly outperform a linear baseline and provide insights into the features that drive song popularity.  

---

## 📊 Dataset  
- **Source:** Kaggle’s [Ultimate Spotify Tracks Dataset (Hamidani, 2019)](https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db)  
- **Size:** ~232,000 songs  
- **Features:** 18 attributes, including:  
  - *Audio features*: danceability, energy, loudness, speechiness, acousticness, instrumentalness, liveness, valence, tempo, duration_ms  
  - *Metadata*: genre, release year  
- **Target Variable:** Popularity score (0–100)  

---

## 🧹 Data Preparation  
- Removed duplicate tracks  
- Handled missing values (imputation & drops)  
- Checked and addressed outliers (e.g., tempo, duration)  
- Ensured consistent data types  

---

## 📈 Exploratory Data Analysis  
- Popularity distribution is **skewed**: most songs are low-popularity, with few hits at the top end.  
- Correlation heatmap highlighted relationships between features.  
- Features like energy, danceability, and valence showed stronger associations with popularity.  

---

## 🤖 Modeling  
Three models were tested:  
1. **Linear Regression**  
   - Baseline model  
   - Underfit the data, reflected in low R² and higher errors  
2. **Random Forest Regressor** (with randomized search)  
   - Captured nonlinear interactions  
   - Improved accuracy over baseline  
   - Provided feature importance insights  
3. **HistGradientBoosting Regressor**  
   - Performed best overall  
   - Iterative boosting refined predictions beyond Random Forest  

---

## 🔑 Key Findings  
- **Tree-based ensemble models** outperformed Linear Regression.  
- **Energy, danceability, and valence** were the strongest predictors of popularity.  
- Extreme popularity scores remain difficult to predict, suggesting that audio features alone do not fully explain success.  

---

## 🚀 Future Work  
- Incorporate **lyrics, playlist placements, and social engagement data** to improve predictions.  
- Experiment with additional models (e.g., XGBoost, LightGBM, CatBoost).  
- Explore classification framing (e.g., predicting “hit” vs “non-hit”).  

---

## 📂 Repository Structure  
- `Spotify_Song_Popularity_Prediction_Project.ipynb` → Main notebook (data cleaning, EDA, modeling, results)  
- `Supervised Learning Rubric.pdf` → Grading rubric  
- `Spotify Song Popularity Project.pptx` → Presentation slides  
- `README.md` → This file  

---

## 🎥 Video Presentation  
A video walkthrough (5–15 minutes) accompanies this project, summarizing the highlights:  
1. Problem definition  
2. ML approach  
3. Results and insights  

---

## 📜 License  
This project is for educational purposes only. Dataset provided under Kaggle’s terms of use.  
