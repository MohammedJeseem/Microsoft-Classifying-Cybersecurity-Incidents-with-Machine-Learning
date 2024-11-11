# Microsoft - Classifying Cybersecurity Incidents with Machine Learning

## Incident Data Analysis and Classification

This project focuses on analyzing and classifying incident data for better incident management. Using a dataset of incidents with features such as timestamps, category, incident grade, and more, the project involves data exploration, preprocessing, and classification modeling to predict incident grades effectively. 

### 1. Data Exploration and Understanding

#### Initial Inspection
- Loaded and inspected the dataset structure to understand variable types, distributions, and missing values.
- Analyzed basic dataset characteristics such as the number of observations, variables, and column names.

#### Exploratory Data Analysis (EDA)
- **Numerical & Categorical Summary**: Generated descriptive statistics for numerical variables and distribution counts for categorical variables.
- **Correlation Analysis**: Visualized correlations between numerical variables to identify key relationships.
- **Missing Values**: Identified and imputed missing values; dropped columns with high null percentages.
- **Class Imbalance**: Assessed class distribution for the `IncidentGrade` target variable and applied stratified sampling for balanced training and validation splits.

### 2. Data Preprocessing

- **Feature Engineering**: Extracted day, month, year, hour, and time from timestamps; encoded categorical variables using Label Encoding.
- **Removing High Null Columns**: Dropped columns with more than 50% missing values, redundant or highly correlated features to enhance model performance.
- **Encoding Categorical Variables**: Applied Label Encoding and filled missing values using appropriate statistical methods.

### 3. Model Building and Evaluation

#### Model Training
- **Baseline Model**: Logistic Regression for initial performance benchmarks.
- **Advanced Models**: Random Forest, XGBoost, and LightGBM were trained and evaluated using accuracy and classification reports.
- **Class Imbalance Handling**: Used `class_weight=balanced` in Random Forest and implemented SMOTE for synthetic sample generation to improve model performance on minority classes.

#### Model Evaluation
- **Performance Metrics**: Computed accuracy, precision, recall, and macro-F1 scores for model evaluation.
- **Cross-Validation**: Used k-fold cross-validation to validate the consistency of model performance.
- **Error Analysis**: Utilized confusion matrices to identify common misclassifications and calculate incorrect prediction percentages.

### 4. Model Interpretation

- **Feature Importance**: Analyzed feature importance to understand influential variables in incident classification.
- **Permutation Importance**: Used permutation importance to observe how shuffling features impacted model performance.

### Results
- The Random Forest model with SMOTE provided the highest accuracy and balanced performance across classes.
- Key features identified were Incident Category, Time, and City.

### Conclusion

This project demonstrates an effective approach for analyzing and classifying incident data. By focusing on data preprocessing, feature engineering, and robust modeling techniques, it provides a scalable solution to predict incident grades accurately, which could enhance incident response and management. 
