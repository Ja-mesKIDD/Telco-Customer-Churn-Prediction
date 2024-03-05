# Telco Customer Churn Prediction
## Overview
This project focuses on predicting customer churn in a telecommunications company through machine learning. Leveraging a dataset encompassing diverse customer interactions and service-related features, the objective is to construct predictive models identifying customers at risk of churning and offer actionable insights for retention.

## Dataset
The Telco Customer Churn dataset, loaded from a provided CSV file, includes features like tenure, internet service type, contract details, and monthly charges. Initial exploration involves showcasing the first 10 rows, assessing data types, null values, unique values, and statistical summaries.

## Data Preprocessing
### Handling Missing Values
Missing values are addressed by imputing constant values, ensuring a clean dataset for analysis and model training.

### Feature Engineering
A new DataFrame (tcl) is created with selected features for subsequent analysis and modeling.

### Categorical Encoding
Binary encoding for categorical features is implemented using the BinaryEncoder from the category_encoders library.

### Preprocessing Pipeline
A comprehensive preprocessing pipeline, employing ColumnTransformer, is constructed to apply different transformations to various feature subsets. This encompasses one-hot encoding, binary encoding, and robust scaling.

## Exploratory Data Analysis (EDA)
Visualizing data enables exploration of relationships and patterns, providing insights into customer behavior and characteristics.

## Modeling
### Sampling Methods
Various sampling methods, including Random Over-sampling, SMOTE, and NearMiss, address class imbalance.

### Model Selection
Exploration of classification models involves Random Forest, K-Nearest Neighbors (KNN), Decision Tree, Ball Tree, and Naive Bayes.

### Hyperparameter Tuning
Grid search optimizes model hyperparameters, utilizing cross-validation with recall as the primary scoring metric.

## Model Evaluation
Models are evaluated based on average recall scores and weighted F1 scores, achieving a balance between sensitivity and precision.

## Results
A summary of grid search results highlights the best parameters and model performance metrics.

## Model Testing
The best-performing model undergoes testing on the test set, providing a detailed classification report, confusion matrix, and a heatmap visualizing the confusion matrix.

## Summary & Recommendations
Exploration into predicting customer churn using Gaussian Naive Bayes models and K-Nearest Neighbors with various sampling methods yields nuanced insights.

### Gaussian Naive Bayes Models:
- Random Over-sampling and SMOTE exhibit comparable results, emphasizing model robustness.
- Despite a moderate overall accuracy (68%), the models excel in accurately identifying potential churn cases, as seen in the impressive 90% recall for the positive class ('Yes' churn).

### K-Nearest Neighbors Model:
- Random Over-sampling demonstrates a distinct advantage, achieving the second-highest recall of 79% for the positive class.
- A balanced trade-off results in an accuracy of 70%, positioning this model as a promising choice for churn prediction.

### Model Comparison:
- While models exhibit similar accuracy, variations in precision and recall underscore the importance of aligning the chosen model with specific business objectives.
- Iterative hyperparameter tuning and exploration of different sampling techniques offer a nuanced understanding of model behavior.

### Recommendations:
- **Preferred Model:** The K-Nearest Neighbors model with Random Over-sampling is the preferred choice due to its commendable balance in capturing actual churn instances without compromising overall accuracy.
- **Business Alignment:** Emphasis on optimizing recall aligns with the focus on detecting churning customers, crucial for proactively addressing customer attrition. The cost of a false negative outweighs that of a false positive in this context.
- The preferred model and emphasis on recall may vary based on specific business visions and goals, considering the ramifications of false positives in different scenarios.

### Insights from Metrics:
- Precision and recall showcase the model's ability to correctly classify positive instances, emphasizing the necessary balance for effective churn prediction.
- The confusion matrix provides detailed insights into the distribution of true positives, true negatives, false positives, and false negatives, offering a nuanced understanding of model performance.

### Note on Hyperparameter Tuning:
- Meticulous hyperparameter tuning, as illustrated, is effective with limited data. For larger datasets, alternative methods like Bayesian optimization or random search may be considered for efficient exploration.

### Conclusion:
The iterative nature of model evaluation and selection underscores the importance of aligning the chosen model with statistical metrics and overarching business goals. The chosen model serves as a valuable asset in identifying and mitigating customer churn.
