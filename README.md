# Cervical Cancer Risk Prediction Model

This repository contains a machine learning model for predicting the risk of cervical cancer based on behavioral, social, and personal health-related data. The goal of the model is to help identify individuals at higher risk of cervical cancer using various socio-behavioral attributes.

## Project Overview

This project applies **Logistic Regression** to predict the likelihood of cervical cancer (`ca_cervix`) based on multiple behavioral, emotional, and social support factors. The dataset includes attributes such as **sexual risk behavior**, **eating habits**, **social support**, **motivation**, and **empowerment**.

The model is trained on a preprocessed dataset, and features are normalized to ensure equal treatment of all variables.

## Dataset

The dataset used in this project is the **sobar-72.csv** file, which contains the following columns:

- **behavior_sexualRisk**: Sexual risk behavior score
- **behavior_eating**: Eating habits score
- **behavior_personalHygine**: Personal hygiene score
- **intention_aggregation**: Intention aggregation score
- **intention_commitment**: Commitment to health-related behaviors
- **attitude_consistency**: Consistency of attitudes toward health
- **attitude_spontaneity**: Spontaneity of health-related attitudes
- **socialSupport_emotionality**: Emotional support score
- **socialSupport_appreciation**: Appreciation of social support score
- **socialSupport_instrumental**: Instrumental support score
- **empowerment_knowledge**: Knowledge empowerment score
- **empowerment_abilities**: Abilities empowerment score
- **empowerment_desires**: Desires empowerment score
- **motivation_strength**: Strength of motivation score
- **motivation_willingness**: Willingness to engage in healthy behaviors
- **ca_cervix**: Binary target variable (0 = No cancer, 1 = Cancer detected)

## Model

The following steps were performed during the project:

1. **Data Preprocessing:**
   - Data cleaning and creation of composite scores (e.g., empowerment_score, socialSupport_score, motivation_score).
   - Normalization of features to a [0,1] range.
   - Removal of unnecessary or highly correlated features.

2. **Model Development:**
   - Split the data into training and testing sets.
   - Trained a **Logistic Regression** model.
   - Evaluated the model using metrics like accuracy, confusion matrix, ROC-AUC, and classification report.

3. **Evaluation Metrics:**
   - **Accuracy**: 0.8667
   - **ROC AUC**: 0.9545
   - **Precision, Recall, F1-score**: Computed for both classes (0: No Cancer, 1: Cancer).

## Results

The Logistic Regression model demonstrated good predictive performance with an accuracy of **86.67%** and a high **ROC AUC score of 0.9545**. The model’s precision and recall indicate it performs well, especially in distinguishing between patients with and without cervical cancer.

## Steps to Run

1. Clone the repository to your local machine:
2. Install the required libraries:
3. Run the model:
  ```bash
  python cervical_cancer_prediction.ipynb
  ```

## Dependencies

- `pandas`
- `numpy`
- `scikit-learn`
- `seaborn`
- `matplotlib`
- `statsmodels` (for VIF)

## License

This project is licensed under the **MIT License**.

## Acknowledgements

- This project was inspired by research in the field of predictive health modeling.
- Special thanks to the open-source community for the tools and libraries that make this work possible.
