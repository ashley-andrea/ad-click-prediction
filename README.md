# Predicting Advertisement Clicks Based on Consumer Profiles
-----
### Project Overview
This project aims to predict whether a consumer will click on an online advertisement based on various features derived from the consumer's profile and their online activity. The dataset, obtained from Kaggle, includes information about online consumer purchasing habits, demographic data, and advertisement interaction data. The target of this binary classification task is to determine if a consumer will click on an ad (1) or not (0), using machine learning techniques.

### Dataset Features
The dataset includes the following features:

- **Daily Time Spent on Site**: Average time (in minutes) that a consumer spends on the website daily.
- **Age**: The age of the consumer.
- **Area Income**: The average income of the consumer's geographical area.
- **Daily Internet Usage**: Average time (in minutes) that the consumer spends on the internet daily.
- **Ad Topic Line**: The headline of the advertisement.
- **City**: The city where the consumer resides.
- **Male**: Binary feature indicating the consumer’s gender (1 for male, 0 for female).
- **Country**: The country where the consumer resides.
- **Timestamp**: The exact time at which the consumer interacted with the advertisement. Format: `YYYY-MM-DD HH:MM:SS`.
- **Clicked on Ad**: The target variable, where 1 indicates the consumer clicked on the advertisement, and 0 indicates they did not.

### Project Workflow
1. **Exploratory Data Analysis (EDA):**

- > **Data visualization:** Several plots were created to understand feature distributions and relationships:
- >> `distplot`, `pair plot`, and `histograms` to visualize distributions of numerical features.
- >> Analysis of relationships between the features and the target variable (`Clicked on Ad`).
- > **Handling missing values:** Missing data was identified and imputed as part of data preprocessing.

2. **Custom Data Transformations:**

> - A custom transformer was built to extract meaningful information from the `Timestamp` feature (e.g., hour of the day, day of the week).

3. **Data Preprocessing:**

> - Features were scaled, categorical variables were encoded, and unnecessary columns were removed.
> - The dataset was split into training and test sets to ensure robust evaluation.

4. **Model Training:**

> - A baseline **Logistic Regression** model was trained first to evaluate initial performance.
> - Cross-validation with Randomized Search was employed to tune the hyperparameters of the model.

5. **Model Selection:**

> - The best model from the cross-validation process was selected based on performance metrics such as accuracy and ROC-AUC score.

6. **Evaluation:**

> - Learning curves and validation curves were plotted to check for overfitting or underfitting.
> - A confusion matrix was generated to better understand the classification results.

### Results
The final model achieved a balanced trade-off between precision and recall, showing good performance in predicting whether consumers will click on an advertisement. Key evaluation metrics and insights from confusion matrices and learning curves were presented to explain the results in detail.

### Conclusion
This project demonstrates a complete machine learning pipeline for a binary classification task, from EDA to model evaluation. It highlights the use of logistic regression with cross-validation for hyperparameter tuning and uses insightful visualizations to support the model's interpretability.
