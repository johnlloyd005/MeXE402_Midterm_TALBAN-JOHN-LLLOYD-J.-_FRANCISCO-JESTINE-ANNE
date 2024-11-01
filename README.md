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
### Customer Satisfaction 
- **Dataset Source:**
- https://www.kaggle.com/datasets/ahmedaliraja/customer-satisfaction-10k
- **Features:** (independent variables)
- Customer - Customer ID
- Delivery Experience
- Food Quality
- Time
- Correct Order - Yes = 1, No = 0
-  **Target Variable:** (dependent variable)
-  Accuracy - Yes = 1, No = 0
-  **Preprocessing Steps:** (data cleaning)
-  To start, I examined my dataset and found that several rows had missing values. To keep the analysis consistent and manageable, I opted to replace these missing values with zeros. Using Python, I loaded the dataset into a Pandas DataFrame and identified the gaps. Then, I applied the fillna() function to substitute the missing values with 0. This approach allowed me to maintain the dataset’s structure while also preparing it for further analysis and calculations.
-  To improve data usability, I modified the "Accuracy" column in my dataset by converting the text values into numerical ones. Specifically, I set Yes = 1 and No = 0. This adjustment not only standardizes the data but also makes it more compatible with machine learning algorithms, which generally perform better with numerical inputs. By replacing text with numbers, I minimized potential processing issues and ensured the data is more efficient for both analysis and model training.

     ![image](https://github.com/user-attachments/assets/45904653-415c-406f-b6b2-a429e870dd2f)

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

### Logistics Regression:
- **Objective 1:** Data Preprocessing: Encode categorical variables, balance classes if needed.
- **Objective 2:** Model Implementation: Use appropriate libraries (e.g., Scikit-learn in Python).
- **Objective 3:** Evaluation Metrics: Calculate Accuracy
- **Objective 4:** Visualization: Plot confusion matrices
- **Objective 5:** Interpretation: Discuss the model's ability to classify and the importance of features.

---

## 4. Methodology

### Logistic Regression Steps:
- Preprocess data for logistic regression.
- Train the logistic model and predict outcomes.
- Evaluate classification performance using confusion matrix and ROC curve.
- Adjust the decision threshold to optimize model accuracy if necessary.

---

## 5. Results and Discussion

- **Data Preprocessing and Feature Engineering:**
- Coverted the "Accuracy" column to numerical values ( 1 for Yes and 0 for No)

  ![image](https://github.com/user-attachments/assets/15656d1f-e04c-4939-bb7d-9af802e2754a)

- To address gaps in the dataset, missing values in key columns were filled with zeros.

  ![image](https://github.com/user-attachments/assets/62105ea8-518c-4263-b3e7-369cbfcd88d9)

- **Modeling and Training:**
- Used Logistic Regression as the primary model for binary classification, with data split into training and testing sets.

  ![image](https://github.com/user-attachments/assets/08ba742b-ec61-4467-b576-3d2b0d2eeec8)
  ![image](https://github.com/user-attachments/assets/121e0cd6-7d13-40ea-a830-441c1f9a5bf6)
  ![image](https://github.com/user-attachments/assets/4ad133a2-b475-4cf6-914a-6adc78f21b4b)
  
- Standardized feature values using StandardScaler to enhance model performance.

  ![image](https://github.com/user-attachments/assets/2593647a-3dfe-4dc5-a268-7a53051840b9)
  
- Generated predictions on the test set using the trained model.

   ![image](https://github.com/user-attachments/assets/8f32c874-de04-435f-9182-74286b0c02bd)

- Created a confusion matrix heatmap to represent the classification performance visually.

  ![image](https://github.com/user-attachments/assets/6ff615bd-f7c8-409e-a868-3a7f0afd9f24)

- Calculated model accuracy based on correct predictions.
![image](https://github.com/user-attachments/assets/3e150c5c-1fb8-42cd-b263-fd6c279b8cc0)




   




- **Data Preprocessing and Feature Engineering:**
  - Converted the 'Sex' column to numerical values (1 for male and 0 for female).
  
  ![image](https://github.com/user-attachments/assets/94e50554-b1b6-4ed5-b697-881e24534992)
  
  - Filled missing values in columns, particularly 'Age,' using median values, and swapped values between 'Pclass' and 'Age' for processing.
    
  ![image](https://github.com/user-attachments/assets/8c69357d-8cf0-4857-8c14-86763c478e18)

  - Calculated correlations between independent variables and the target variable 'Survived,' displaying the correlation values in a bar chart.
    
  ![image](https://github.com/user-attachments/assets/f5ed25a6-22e4-4a6f-b1eb-beb50c85fb39)

  ![image](https://github.com/user-attachments/assets/bdfca8ef-c079-42ac-a768-a112ae50b3cf)
    
- **Gender-based Survival Rate::**
  -  Calculated and printed the survival rates separately for female and male passengers.
    
  ![image](https://github.com/user-attachments/assets/4f306006-4249-4de9-abd3-1271e5b999a9)
  
- **Modeling and Training:**
  - Used Logistic Regression as the primary model for binary classification, with data split into training and testing sets.

![image](https://github.com/user-attachments/assets/c22723a3-890a-4969-8429-3c8ebdb64e69)

![image](https://github.com/user-attachments/assets/ff10906c-002a-4b91-bb35-8fb358c26a55)

![image](https://github.com/user-attachments/assets/52f9c44a-c5d2-4463-a3e3-b3e5ceedb2f4)
  
  - Standardized feature values using StandardScaler to enhance model performance.

![image](https://github.com/user-attachments/assets/ac412c60-538d-4e34-9287-c6c244ace536)
    
  - Generated predictions on the test set using the trained model.
  
- **Visualization and Performance Evaluation:**
  - Visualized the true and predicted class labels for two primary features to compare accuracy.
 
![image](https://github.com/user-attachments/assets/29b0b7d5-37fe-4220-b42e-f734ac053d96)
**X-axis (Feature 1):** This is the first feature (or dimension) from the dataset X_test. It’s one of the five features generated in the synthetic data but is plotted independently to provide a visual representation of how the two classes are distributed based on just this feature.

**Y-axis (Feature 2):** This is the second feature from X_test. Like Feature 1, it’s plotted to show its influence on the binary classification outcome when combined with Feature 1.

  - Created a confusion matrix heatmap to represent the classification performance visually.

![image](https://github.com/user-attachments/assets/e4809f88-b38f-465f-a4f2-0da1c3d097db)

  - Calculated model accuracy based on correct predictions.

![image](https://github.com/user-attachments/assets/987602a7-a73e-42e7-bcfb-2687994aa4e7)

---


## 6. Conclusion

In conclusion, the objectives outlined guided a structured approach to building a classification model. By first encoding categorical variables and balancing classes, we ensured that the data was in a suitable format for training and evaluation. Using Scikit-learn, we implemented and fine-tuned a model that could effectively classify the data, and calculated its accuracy to gauge initial performance. Visualizing confusion matrices provided insights into classification accuracy for each class, highlighting any areas where the model struggled. Finally, interpreting the model's classifications and feature importance allowed us to understand which features were most impactful, supporting both the model’s validity and its potential areas for improvement. This end-to-end approach optimized model performance and interpretability.

---

## 7. References
UCI Machine Learning Repository
Scikit-learn User Guide
ResearchGate


- https://www.kaggle.com/code/alexisbcook/titanic-tutorial
- https://www.kaggle.com/code/gusthema/titanic-competition-w-tensorflow-decision-forests
- https://www.kaggle.com/datasets/ahmedaliraja/customer-satisfaction-10k
- https://huggingface.co/blog/supercharge-customer-service-with-machine-learning
