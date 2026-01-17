🍄 Mushroom Identification Using Machine Learning

This project applies machine learning techniques to classify mushrooms as edible or poisonous based on their physical characteristics.
It follows a complete end-to-end data science workflow, from data preprocessing and model development to evaluation, visualization, and presentation.

📌 Project Overview

Correctly identifying poisonous mushrooms is a safety-critical classification task.
This project explores multiple machine learning models and evaluation strategies to minimize dangerous misclassifications, particularly cases where poisonous mushrooms are incorrectly labeled as edible.
The dataset consists entirely of categorical features and is well suited for tree-based and ensemble learning methods.

📂 Repository Structure

mushroom-identification-final.ipynb
Final Jupyter Notebook containing:
  Data preprocessing
  Feature engineering
  Model training
  Hyperparameter tuning
  Model evaluation
  Visualizations
  README.md
  Project documentation

🧠 Dataset

Source: Mushroom dataset (UCI)
Samples: 8,124 mushrooms
Features: Categorical physical attributes
Target variable:
  0 → Edible
  1 → Poisonous
Missing Values:
  Missing data was found in the stalk-root feature.
  Missing values were handled by introducing a dedicated category ("m"), preserving potentially informative patterns rather than removing samples.

🔧 Data Preprocessing & Feature Engineering

Replacement of missing values with an explicit category
One-hot encoding of all categorical features
drop_first=True used to avoid multicollinearity
Train/test split with stratification to preserve class balance

🤖 Models Implemented

The following models were trained and evaluated:
  Logistic Regression (baseline model)
  Decision Tree Classifier
  Unrestricted tree
  Depth-limited tree (max_depth)
  Random Forest Classifier (ensemble model)

🔍 Hyperparameter Tuning

Hyperparameter tuning was performed using Grid Search with Cross-Validation, focusing on:
  Decision Tree
  max_depth
  min_samples_split
  min_samples_leaf
  Random Forest
  n_estimators
  max_depth
  min_samples_leaf

Cross-validation ensured that model performance was robust and not dependent on a single train–test split.

📊 Evaluation Strategy

Model performance was evaluated using:
  Accuracy
  Precision, recall, and F1-score
  Confusion matrices

Special attention was given to false negatives for the poisonous class, as misclassifying a poisonous mushroom as edible represents a critical safety risk.

🏆 Key Results

Logistic Regression achieved high accuracy but produced a small number of dangerous misclassifications.
Decision Trees showed sensitivity to depth constraints, illustrating the bias–variance tradeoff.
Random Forest achieved perfect classification on the test set, eliminating all poisonous-to-edible errors.
The Random Forest model was selected as the final model due to its robustness and superior safety performance.

📈 Feature Importance

Feature importance analysis revealed that a small number of features drive most predictions, including:
  Odor
  Spore print color
  Gill characteristics

These findings are consistent with known biological indicators of mushroom toxicity.

📊 Dashboard

An interactive dashboard was created using Tableau to explore the dataset and visualize key patterns.

🔗 Tableau Dashboard:
https://public.tableau.com/app/profile/rui.braz/viz/MushroomsAnalysis/Dashboard1?publish=yes

🎤 Presentation

A project presentation summarizing methodology, results, and conclusions is available here:

🔗 Presentation (Canva):
https://www.canva.com/design/DAG92-k1V3c/XLmJefX_0byoNwCHGtra7Q/edit

⚠️ Limitations & Ethics

The dataset is clean and curated; real-world mushroom identification is more complex.
Models trained on this dataset should not replace expert judgment.
Machine learning systems should be used as decision-support tools, especially in safety-critical domains.

🚀 Technologies Used

Python
pandas, numpy
scikit-learn
matplotlib
Jupyter Notebook
Tableau
Canva

👤 Author

Camilla Scandola
Rui Braz
Machine Learning Project – Mushroom Identification

📄 License

This project is intended for educational and academic purposes.
