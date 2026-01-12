# ML_Final  
## Mushroom Edibility Classification (Tabular Machine Learning)

**Course:** Introduction to Machine Learning (2025–2026) – Final Project  
**Authors:**  
- Yusuf Eren Aykurt (1306210062)  
- İsmail Çolak (1306210024)

---

## Problem Definition
This project addresses a binary classification task: predicting whether a mushroom is edible (e) or poisonous (p) based on morphological and environmental attributes. The goal is to evaluate classical machine learning models on tabular data with an emphasis on safety-critical classification.

---

## Dataset
**Secondary Mushroom Dataset (UCI Machine Learning Repository)**  
https://archive.ics.uci.edu/dataset/848/secondary+mushroom+dataset  

- Type: Tabular (categorical + numerical features)  
- Target variable: `class`  
  - p → 1 (poisonous)  
  - e → 0 (edible)  

---

## Repository Structure
ML_Final/
├── mushroom_classification.ipynb
├── requirements.txt
└── data/
    └── secondary_data.csv


---

## Install Dependencies
pip install -r requirements.txt


### Run the Notebook

**VS Code:**  
Open `mushroom_classification.ipynb` and click **Run All**

**Jupyter Notebook:**  
Then open the notebook and run all cells.

---

## Reproducibility Notes
- 80/20 train–test split with `random_state=42` and stratification.
- All preprocessing steps are implemented using a single scikit-learn Pipeline to prevent data leakage.
- Random Forest hyperparameter tuning is performed using GridSearchCV with 3-fold cross-validation on the training set.
- F1-score is used as the primary optimization metric due to the safety-critical nature of the problem.

---

## Evaluation
Model performance is evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrices
- ROC Curves

Special emphasis is placed on precision and recall for the poisonous class, as misclassifying a poisonous mushroom as edible carries significant risk.

---

## Notes
This repository is intended for educational and academic purposes as part of a university-level machine learning course.
