# 🎓 Online Learning Completion Prediction System

## 🧩 Problem Statement

Online education platforms face major challenges with student **retention** and **course completion**. Most systems lack:

- Predictive capabilities to identify at-risk students early  
- Insights into engagement patterns affecting course outcomes  
- Tools for automated, personalized interventions

This project addresses these challenges by building a machine learning model to predict a student's likelihood of completing an online course based on their engagement data.

---

## 🎯 Project Objectives

1. Build a predictive model with **>80% accuracy**  
2. Identify key **behavioral indicators** of course completion  
3. Generate **interpretable** insights for educators  
4. Create a **scalable** solution that can integrate with existing LMS platforms  
5. Ensure **academic compliance** with Integral University guidelines  

---

## 🧠 Methodology

### 1. Data Collection & Preparation

#### 📊 Dataset Description:
Used a dataset of **100 student records** with the following features:

- **`videos_watched`** – Number of videos watched  
- **`assignments_submitted`** – Number of assignments submitted  
- **`forum_posts`** – Number of forum interactions  
- **`completion_status`** – Target variable (`1` = Completed, `0` = Not Completed)

#### 🧹 Preprocessing Steps:
- **Missing Values:** Imputed using the **median**  
- **Target Conversion:** Encoded `completion_status` as binary  
- **Normalization:** Applied **StandardScaler** for numerical features

---

### 2. Feature Engineering

#### 📈 a. Total Engagement Score
Calculated by summing student activities:
```python
df['total_engagement'] = (
    df['videos_watched'] +
    df['assignments_submitted'] +
    df['forum_posts']
)
