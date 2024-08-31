# IBM HR Analytics Employee Attrition & Performance



## Business Understanding
IBM is a global technology and consulting firm that operates in a highly competitive and dynamic market. Effective human capital management is critical for sustaining market leadership and meeting business objectives. Employee attrition and performance are critical factors in determining organisational success. High turnover rates can disrupt team dynamics, increase recruitment and training costs, and potentially limit innovation and productivity. In contrast, retaining top performers and effectively managing employee performance can boost business growth and operational efficiency.



## Data Understanding

The IBM HR Analytics dataset used in the analysis includes various employee-related attributes aimed at understanding factors influencing employee attrition and performance. The dataset contains features such as age, gender, job role, department, daily rate, distance from home, education level, job satisfaction, work-life balance, and monthly income. The objective is to analyze these factors to identify key drivers of attrition, understand the impact of work environment and performance on retention, and develop predictive models to anticipate future attrition trends.

### Objectives
Objective:

The primary objective is to analyze the available HR data to uncover insights into the factors driving employee attrition and performance at IBM. By leveraging this data, the project aims to:

. Identify key drivers of attrition across different segments of the workforce.

. Understand the relationship between employee performance metrics and attrition rates.

. Assess the impact of work environment factors on retention and job satisfaction.

. Create predictive models to anticipate future attrition trends and support proactive HR interventions.

## Modelling

### Data Preprocessing
Encoding Categorical Variables:
The dataset contained categorical features such as Department, JobRole, EducationField, etc. These variables are converted into numerical format using techniques like One-Hot Encoding. This process ensured that the machine learning algorithms can interpret these features correctly.


### Model Building
Logistic Regression:
Logistic Regression is used as a baseline model due to its simplicity and interpretability. This model is particularly useful for binary classification problems like predicting whether an employee will leave (Yes) or stay (No). It estimated the probability of the attrition based on the input features.
The coefficients from the Logistic Regression were interpreted to understand the impact of each feature on the probability of attrition.


Random Forest:
A Random Forest model is built by combining multiple decision trees, each trained on different subsets of the data and features. The ensemble method improved model accuracy through reducing variance, which typically leads to overfitting in decision trees.
also Random Forests, helped to identify which variables were most influential in predicting attrition.


## Model Evaluation
Precision, Recall, F1-Score:
Given the potential imbalance in the dataset , metrics like Precision, Recall, and F1-Score were crucial for assessing model performance.
Precision measured the accuracy of positive predictions, Recall measured the ability to identify all positive instances, and F1-Score is the harmonic mean of Precision and Recall.

## Conclusion
Model Performance Summary:

Accuracy: 83.67%
Precision: 52.38%
Recall: 22.45%
F1 Score: 31.43%
### 1. Overall Accuracy:

The Decision Tree model has a high accuracy of 83.67%, indicating that it performs well in correctly predicting both attrition and non-attrition cases overall.
### 2. Precision:

With a precision of 52.38%, the model is moderately effective at identifying instances of attrition when it predicts them. This means that about half of the instances flagged as attrition are true positives. However, there is a considerable proportion of false positives, where the model incorrectly labels non-attrition cases as attrition.
### 3. Recall:

The recall of 22.45% is relatively low, indicating that the model identifies only a small fraction of actual attrition cases. This suggests that many employees who are likely to leave are not being flagged by the model, which could be problematic if the goal is to proactively address potential attrition.
### 4. F1 Score:

The F1 Score of 31.43% reflects a balance between precision and recall, but the low score highlights that the model struggles to effectively capture the positive cases (attrition) while maintaining a reasonable level of precision.
Implications
Attrition Identification: The model's ability to identify attrition is limited, as evidenced by the low recall. This means the organization may be missing many potential cases of employee attrition, which could affect planning and retention strategies.

## Recommendations:

### Improve Recall: 
Focus on improving the model's recall to ensure that more actual attrition cases are identified. This can be achieved by addressing class imbalance, adjusting the classification threshold, and exploring advanced models.
### Feature Engineering: 
Enhance the feature set to better capture the factors contributing to attrition. This could involve adding new features or refining existing ones based on domain knowledge.
### Model Enhancement:
Consider experimenting with different algorithms and hyperparameter tuning to improve the model's performance metrics.
## Strategic Recommendations:

### Proactive Measures:
Implement strategies to address the factors contributing to attrition more effectively, using insights gained from refining the model.
### Advanced Techniques:
Explore ensemble methods or other machine learning techniques to achieve better performance in predicting employee attrition.