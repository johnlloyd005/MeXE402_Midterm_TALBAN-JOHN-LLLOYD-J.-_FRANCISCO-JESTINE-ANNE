# MeXE402_Midterm_TALBAN-JOHN-LLLOYD-J.-_FRANCISCO-JESTINE-ANNE
# Linear and Logistic Regression Analysis

## 1. Introduction

### Overview of Linear Regression:
Linear regression is a statistical method used to model the relationship between a dependent variable and one or more independent variables. The goal is to find a linear equation that best predicts the dependent variable from the independent variables. This method assumes a linear relationship between the variables and minimizes the error (residual sum of squares) between observed and predicted values. Key elements include determining how independent variables influence the dependent variable, generating a line of best fit for prediction, and ensuring that certain assumption like linearity and independence are met for accurate results.

Applications of linear regression include predicting continuous outcomes such as prices, temperatures, or other measurable quantities.

### Overview of Logistic Regression:
Logistic regression, unlike linear regression, is used for binary or categorical outcome prediction. Instead of predicting a continuous value, it estimates the probability that a given input belongs to a certain class, typically by using a logistic function to model the data. The output is a probability score between 0 and 1, which is later classified into one of the two classes based on a threshold value. Logistic Regression also handles binary classification (such as yes/no, true/false outcomes) and can be extended to multiclass classification using techniques. (e.g., 0.5).

Logistic regression is often used for classification tasks such as spam detection, disease diagnosis, or churn prediction.

---

## 2. Dataset Description

### Titanic - Machine Learning from Disaster:
- **Dataset Source:**
  -  https://www.kaggle.com/c/titanic/data
- **Features:** (independent variables)
  - pclass - Ticket class	1 = 1st, 2 = 2nd, 3 = 3rd
  - Sex Male = 1 Female = 0
  - Age -	Age in years
  - sibsp -	No. of siblings / spouses aboard the Titanic
  - parch -	No. of parents / children aboard the Titanic	
- **Target Variable:** (dependent variable)
  - survival - Survival	0 = No, 1 = Yes
- **Preprocessing Steps:** (data cleaning)
  - As I delved into my dataset, I noticed that many cells in the "age" column were missing values. To ensure that my analysis could proceed smoothly, I decided to fill these missing entries with zeros. Using 
    Python, I wrote a script that specifically targeted the "age" column. I began by loading my dataset into a Pandas DataFrame. After identifying the missing values, I used the fillna() method to replace them 
    with 0. This not only helped maintain the structure of my data but also made it easier to perform calculations and analyses later on.
  - I converted the "Sex" column in my dataset so that it uses numerical values instead of text. I assigned male = 1 and female = 0. This makes the data more efficient to work with, especially for machine learning 
    models, which perform better with numerical data.

  ![image](https://github.com/user-attachments/assets/6dd7b92c-5e03-492c-940a-ffe93660de33)

---

## 3. Project Objectives

### Editable Outline:
- **Objective 1:** Data Preprocessing: Encode categorical variables, balance classes if needed.
- **Objective 2:** Model Implementation: Use appropriate libraries (e.g., Scikit-learn in Python).
- **Objective 3:** Evaluation Metrics: Calculate Accuracy
- **Objective 4:** Visualization: Plot confusion matrices
- **Objective 5:** Interpretation: Discuss the model's ability to classify and the importance of features.

---

## 4. Methodology

### Linear Regression Steps:
- Split the dataset into training and testing sets.
- Train the model using the training set.
- Evaluate model performance using the testing set.
- Interpret the coefficients of the linear model.

### Logistic Regression Steps:
- Preprocess data for logistic regression.
- Train the logistic model and predict outcomes.
- Evaluate classification performance using confusion matrix and ROC curve.
- Adjust the decision threshold to optimize model accuracy if necessary.

---

## 5. Results and Discussion

- **Linear Regression Results:** Provide an overview of the model performance, the importance of different features, and any insights gained from the regression analysis.
- **Logistic Regression Results:** Discuss the accuracy and reliability of the logistic model, as well as potential improvements or adjustments.
- **Comparison of Models:** Summarize the differences between the models and how they perform for the respective tasks.

---

## 6. Conclusion

- Summarize the key findings from both regression analyses, highlighting the main outcomes
- Discuss the overall effectiveness of linear and logistic regression for the dataset and problem context.
- Suggest potential next steps or improvements for future analyses such as deeper data exploration
- Assess the interpretability of both models for stakeholders, ensuring that the results can be easily understood and applied in decision-making processes.

---

## 7. References
UCI Machine Learning Repository
Scikit-learn User Guide
ResearchGate


- https://www.kaggle.com/code/alexisbcook/titanic-tutorial
- https://www.kaggle.com/code/gusthema/titanic-competition-w-tensorflow-decision-forests
