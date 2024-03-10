

---

# Project - Scikit-Learn Feature Selection, Dimensionality Reduction, and Ensemble Models

## Description
This project focuses on applying machine learning techniques to recognize activities performed by subjects using a smartphone. The dataset used contains measurements collected from 30 subjects in a clinical study, where they were asked to perform daily life activities while wearing a smartphone with inertial sensors. The goal is to classify activities into one of six categories: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, and LAYING. Linear acceleration in 3 axes and angular velocity in those same axes were captured using the phone's accelerometer and gyroscope at a constant frequency of 50 Hz.

Sensor signals were preprocessed using noise filters and sampled with sliding windows of 2.56 seconds and a 50% overlap. Features were extracted in both time and frequency domains. It is important to note that the acceleration signal was filtered to remove the gravity component and retain only body movement.

## Attributes
- Subject identifier
- Triaxial acceleration from the accelerometer (total acceleration) and estimated body acceleration
- Triaxial angular velocity from the gyroscope
- 561 features extracted in time and frequency domains
- Activity label

## Problem Summary
- Number of examples: 10,299
- Number of variables: 561
- Variable types: Integer, Real, and Categorical
- Presence of null values: Yes

## Repository Contents
- **data/**: Folder containing the dataset used in CSV format.
- **code/**: Folder containing the source code used in the project, including scripts for feature selection, dimensionality reduction, and model training.
- **README.md**: This file, providing an overview of the project and its contents.
- **Dataset**: https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones

## Summary of Project:

This project focuses on analyzing a dataset collected from smartphones to recognize human activities. The dataset includes measurements from 30 subjects performing daily life activities while wearing a smartphone with inertial sensors. The goal is to classify these activities into one of six categories: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, and LAYING. The dataset consists of 561 features extracted from accelerometer and gyroscope readings, along with subject identifiers and activity labels.

The project workflow can be summarized as follows:

1. **Data Loading and Basic Description**: The dataset is loaded, and basic statistics such as the number of variables, instances, unique individuals, and output classes are computed and displayed.

2. **Handling Missing Values**: The percentage of null values per variable and in the total dataset is calculated. Techniques like mean imputation for integer variables, KNN imputation for categorical variables, and iterative imputation for real variables are applied to handle missing values.

3. **Data Preprocessing**: Data is prepared for classification techniques by encoding categorical labels, handling missing values, and scaling numeric features using a preprocessing pipeline.

4. **Train-Test Split**: A holdout of 10% of the data is reserved for final validation, ensuring individual-wise splitting to avoid contamination between train and test sets.

5. **Modeling**: Different feature reduction techniques such as ANOVA, Mutual Information, RFE, PCA, and ICA are applied. Models like MLP, KNN, SVM, Bagging, and AdaBoost with SVM are trained using grid search and cross-validation.

6. **Ensemble Models Creation**: Ensemble models including Random Forest, XGBoost, Hard Voting, Soft Voting, and Ensemble Stacking are created using the best performing models from the previous step.

7. **Evaluation and Analysis**: The accuracy of each model is evaluated on the test set. Additionally, the number of variables selected by reduction techniques and the importance of variables selected by Random Forest and XGBoost are analyzed and visualized.

8. **Documentation**: The results and analysis are documented in this Jupyter Notebook, and the notebook is converted to HTML for sharing and presentation purposes.

The project aims to demonstrate the application of machine learning techniques for activity recognition using smartphone sensor data, along with the evaluation and comparison of different models and feature reduction methods.

License
This project is licensed under the MIT License.
---

This README provides an overview of your project, its purpose, the dataset used, attributes, and how to use and contribute to the project. If you need further information or specific adjustments, feel free to ask!