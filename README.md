# Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria

This project is interesting and potentially very beneficial for public health, given the importance of combating the hepatitis C virus among the Egyptian population. Indeed, Egypt is the country experiencing the largest hepatitis C epidemic in the world. According to a statement published on the WHO website, 87% of people living with hepatitis C have been diagnosed, which is a viral liver infection primarily transmitted through blood.

To successfully carry out this project, here are some steps you might consider:

1. Data Collection: Gather a representative dataset of records related to the hepatitis C virus base for Egyptian patients.
2. Data Preprocessing: Clean and prepare the data to make it compatible with machine learning models. This might involve handling missing values, normalizing data, managing outliers, etc.
3. Data Exploration: Perform exploratory data analysis to understand the relationships between different variables. This might help you select the best features for your model.
4. Model Selection: Choose different machine learning methods suitable for classification tasks. Commonly used methods include Support Vector Machines (SVM), Neural Networks, Decision Trees, and ensemble methods like Random Forests.
5. Data Splitting: Split your data into training and test sets. This allows you to evaluate your model's performance on data it has not seen during training.
6. Model Training: Train your models using the training set. Use cross-validation techniques to evaluate performance robustly.
7. Performance Evaluation: Assess the performance of each model using the test set. Use appropriate metrics such as accuracy, recall, F1-score, etc.
8. Interpretation of Results: Understand the decisions made by your model. This is crucial in the medical field to ensure trust from practitioners and patients.
9. Deployment: Once you're satisfied with your model's performance, deploy it in a real-world environment for practical use.

The CRISP-DM Method: CRISP-DM stands for Cross-Industry Standard Process for Data Mining. It is a data mining project management process model that provides a structured approach for planning, implementing, and maintaining data mining solutions. By adapting this methodology, the various steps based on my script will be explained.

![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/4dcffcbf-8c0f-474a-8b95-90aa8b563575)

Project Objective:
The primary goal of this project is to apply various machine learning techniques to learn from and classify records related to the hepatitis C virus database for Egyptian patients. The ultimate aim is to develop classification models capable of predicting the class of the target variable 'Baseline histological staging' based on other medical features.

# Importer les bibliothèques nécessaires :
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/e3aa16cd-13e0-4ddb-9537-00f379cf0074)

# Phase 1: Business Understanding
The business objective is to provide decision support tools for evaluating the histological stage of hepatitis C in Egyptian patients. This would enable a better understanding of the disease's progression and allow for more precise medical management.

# Phase 2: Data Understanding
• Data Collection: The data is extracted from the hepatitis C virus database for Egyptian patients, specifically from the file "HCV-Egy-Data.csv".
• Data Exploration: An analysis of the available features is conducted, including the identification of the classes of the target variable and understanding the relationships between the different variables.

![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/f12a0940-1435-42b9-af2f-5fe97ca801f8)

[1385 rows x 29 columns]
I have a dataset that consists of 1385 rows (or observations) and 29 columns (or variables). This means that each row in your dataset represents an entry or instance, and each column represents a different feature or variable associated with these entries.

# Phase 3: Data Preparation
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/3d9bfb09-a701-4858-a1cd-534d68dbc839)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/08d06530-a839-4a6b-b2bc-ab0274eb357e)

Data Cleaning and Preprocessing Steps:

• Data Cleaning: The values of 5 in certain columns are replaced with NaN, followed by the detection and handling of outliers.

• Imputation: Missing values are imputed using the median.

• Standardization / Normalization: The data is standardized to ensure that all features are on the same scale using StandardScaler from Scikit-learn.

• Feature Selection: Identify and retain the most important features by eliminating redundant or less informative ones using SelectKBest.

• Categorical Variable Encoding: Categorical variables are encoded into numerical forms to be used as inputs in machine learning models using LabelEncoder.

• Class Balancing: Sampling techniques (e.g., SMOTE) are applied if the classes are imbalanced.

# Phase 4: Modeling
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/b9bcd842-1681-492b-a84a-89147eed4c1b)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/57c15c46-1241-4372-a336-907967eeefb0)

Model Creation: Seven classification models are used:

• Random Forest
• SVM (Support Vector Machine)
• Logistic Regression
• Gradient Boosting
• Decision Tree
• K-Nearest Neighbors (KNN)
• Naive Bayes

Cross-Validation: The performance of the models is evaluated using cross-validation with metrics such as:

• Accuracy
• Precision
• Recall
• F1-score
• K-fold cross-validation

# Phase 5: Evaluation
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/6c73918d-b123-48b9-aaf1-57c57f6f64c7)

• Model Evaluation: The results of the models are evaluated for each binary class.

• Performance Comparison: The performance of the models is compared and analyzed for each binary class.

# Phase 6: Deployment:

• Model Saving: The trained models are saved for future use.

# Analysis and Interpretation:
• Binary Class 1.0
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/2247839c-8f3b-4716-aa8a-e5b3bbff7fbd)

• Binary Class 2.0
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/40306c26-49b4-4242-9920-ec19846f131d)

• Binary Class 3.0
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/1e9210a1-af7b-4be1-bf95-253c73acf246)

• Binary Class 4.0
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/19c980a7-4b55-4b6c-8d3f-c53c6ab27f35)


# Conclusion:
* Classification Model:
Binary Class 1.0: 
The performance of the models is relatively similar, with values around 60%, indicating average precision and recall.

Binary Class 2.0: 
The Gradient Boosting model significantly improved performance, reaching approximately 73% in terms of precision, recall, and F1-score. Other models perform between 54% and 65%.

Binary Class 3.0: 
These models show balanced performance with values around 54% to 56%, exhibiting similar precision and recall.

Binary Class 4.0: 
Random Forest and Gradient Boosting show performance around 66% to 67%, while other models achieve modest values around 53% to 56%.

* Confusion Matrix:
A confusion matrix is a table that describes the performance of a classification model on a dataset. It helps visualize the number of correct and incorrect predictions made by the model. Confusion matrices are particularly useful for evaluating the performance of binary classification models. A typical confusion matrix looks like this:
[[164 39]
[ 55 19]]

164 (Top-left): True Negatives (TN) – 164 instances are correctly predicted as negative by the model. These are observations that were actually negative and were correctly classified as such.

39 (Top-right): False Positives (FP) – 39 instances were predicted as positive by the model but were actually negative. These are Type I errors, where the model incorrectly predicted a positive occurrence.

55 (Bottom-left): False Negatives (FN) – 55 instances were predicted as negative by the model but were actually positive. These are Type II errors, where the model missed positive occurrences.

19 (Bottom-right): True Positives (TP) – 19 instances are correctly predicted as positive by the model. These are observations that were positive and were correctly classified as such.

* Confusion Matrix Visualization:
Visualizing the confusion matrix as a heatmap helps us understand the model’s errors. The values are labeled to indicate how frequently each category appears, and colors can be used to highlight differences (e.g., true positives might be colored green, false positives in red, etc.). In the context of the confusion matrix and color visualization:

True Positives (TP): Often displayed in green or blue, indicating the model correctly predicted a positive case.

True Negatives (TN): Often displayed in green or blue, indicating the model correctly predicted a negative case.

False Positives (FP): Often displayed in red or yellow, indicating the model incorrectly predicted the case as positive.

False Negatives (FN): Often displayed in red or yellow, indicating the model incorrectly predicted the case as negative.

# Summary:
The Random Forest model shows consistent performance across all metrics and demonstrates a balanced ability to correctly predict both positive and negative classes.











