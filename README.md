# Liver-Cirrhosis-Stage-Detection


## 📌 Objective
Build a machine learning system that predicts the *level of liver damage* (cirrhosis stage) based on various patient medical attributes collected from a real-world dataset.

---

## 📊 Dataset Overview
- *Source*: Mayo Clinic study on Primary Biliary Cirrhosis (PBC), conducted from 1974–1984.
- *Records*: Patient clinical data including age, gender, symptoms, and various blood and liver test results.
- *Target variable*: Stage (liver cirrhosis stage)

### 🔍 Key Features:
| Column         | Description |
|----------------|-------------|
| N_Days         | Number of days between registration and end point |
| Status         | Patient outcome: C (censored), CL (censored - liver transplant), or D (death) |
| Drug           | Medication given: D-penicillamine or Placebo |
| Age            | Age in days |
| Sex            | M (Male), F (Female) |
| Ascites        | Fluid buildup in abdomen: Y or N |
| Hepatomegaly   | Enlarged liver: Y or N |
| Spiders        | Blood vessel malformations: Y or N |
| Edema          | Fluid retention condition: N, S, or Y |
| Bilirubin      | Serum bilirubin (mg/dl) |
| Cholesterol    | Serum cholesterol (mg/dl) |
| Albumin        | Albumin (gm/dl) |
| Copper         | Urine copper (ug/day) |
| Alk_Phos       | Alkaline phosphatase (U/liter) |
| SGOT           | Liver enzyme (U/ml) |
| Tryglicerides  | Triglycerides (mg/dl) |
| Platelets      | Platelet count (per ml/1000) |
| Prothrombin    | Prothrombin time (sec) |

---

## 🧠 Models Used

1. *Logistic Regression*
   - Baseline linear classifier.
   - Achieved Accuracy: ~51.9%

2. *K-Nearest Neighbors (KNN)*
   - Instance-based learner.
   - Tuned with k=10
   - Accuracy: ~63.3%

3. *Random Forest Classifier*
   - Ensemble model for better generalization.
   - Accuracy: ~68.8%

---

## 🛠 Preprocessing
- Missing values dropped (df.dropna())
- Categorical features label-encoded (e.g., Sex, Edema, Drug)
- Stratified train-test split to preserve class distribution
- Optional: Feature scaling applied for distance-based models

---

## 📈 Results Summary

| Model               | Accuracy |
|--------------------|----------|
| Logistic Regression| ~51.9%   |
| KNN (k=10)         |  ~63.3%  |
| Random Forest      | ~68.8%   |

> Note: Accuracy may vary depending on data cleaning and feature selection.

---

## 📂 Files

- liver_cirrhosis.csv: Original dataset
- Liver_Cirrhosis_Prediction_using_KNN_LogisticRegression&RandomForest.ipynb: Code notebook with preprocessing, training, and evaluation
- README.md: Project documentation

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone <your-repo-link>

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the notebook
jupyter notebook Liver_Cirrhosis_Prediction_using_KNN_LogisticRegression&RandomForest.ipynb
