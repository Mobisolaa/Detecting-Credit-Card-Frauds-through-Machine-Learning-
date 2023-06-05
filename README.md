# Detecting-Credit-Card-Frauds-through-Machine-Learning-
Leveraging supervised learning to predict and prevent fraudulent credit card transactions . 
### Overview
This is a project that utilizes machine learning to determine the legitimacy of credit card transactions. By analyzing a sample of 284807 transactions, patterns can be identified and used to predict future transactions as either fraudulent or legitimate. This is a classification task, as the target variable is categorical (fraud or no-fraud), and various classification models will be tested to determine the most effective one.

- Data Analysis - 
This is to gain understanding of the dataset- to identify patterns in the data and select on the approprate model to achieve the desired outcome. During this stage, it was discovered that the dataset is unbalanced, with one class (legitimate transactions) having more records than the other (fraudulent transactions).

- Data preprocessing - 
To address this issue, the data went through preprocessing to balance the distribution. Classifiers tend to favor the majority class, resulting in errors if the model is trained on unbalanced data. Therefore, a balanced distribution was necessary for optimal learning and prediction accuracy.

- Data Visualization 

![Screenshot 2023-06-05 150736](https://github.com/Mobisolaa/Detecting-Credit-Card-Frauds-through-Machine-Learning-/assets/122166125/867e5bfe-7a1b-41c3-8119-dc4fae3f1161)


- Model Training - 
The model was trained on the balanced dataset and its performance was evaluated using the untouched, unbalanced testing set. This provides a fair evaluation of the model's ability to generalize to real-world, unbalanced data.

![Screenshot 2023-06-05 154902](https://github.com/Mobisolaa/Detecting-Credit-Card-Frauds-through-Machine-Learning-/assets/122166125/507d5fdf-8d73-46f4-864f-f66803ea4870)

- Evaluation - 
Use the classification report of each model to assess their performances. The higher the accuracy, the better a classification model is able to predict outcomes.

It's worth noting that the absence of significant disparities between accuracy scores on the training and testing models suggests no concerns of over or under-fitting.


### Result Analysis

- Logistic Regression

![Screenshot 2023-06-05 154221](https://github.com/Mobisolaa/Detecting-Credit-Card-Frauds-through-Machine-Learning-/assets/122166125/e17becb1-f4b3-4d2d-862d-cca94ff25544)

The model has 100% precision for legitimate transactions, correctly identifying them as not fraudulent. However, it struggles with false positives for fraudulent transactions, incorrectly flagging many legitimate transactions as fraudulent (Predicted only 3% correctly). This could result in a negative customer experience if genuine transactions are continually blocked due to incorrect predictions. 

The recall rate for both legitimate and fraudulent transactions is 95%, meaning the model correctly identifies 95% of actual legitimate and fraudulent transactions.

The F1 score which harmonises the Precision and the Recall indicates a high accuracy for legitimate transactions with a score of 0.98. However, the F1 score for fraudulent transactions is only 0.07, suggesting the model struggles to correctly identify true positives.

The overall accuracy of the model is 0.95, meaning that it correctly classifies 95% of the transactions in the dataset.

Overall, the model accurately classifies 95% of transactions. While it performs well for legitimate transactions, it needs further improvement to better detect fraudulent transactions as indicated by the low precision and F1-score for the Fraud class. Other classification models, such as Random Forest, Shallow, and GBoost, may be worth considering.

- Random Forest

![Screenshot 2023-06-05 154121](https://github.com/Mobisolaa/Detecting-Credit-Card-Frauds-through-Machine-Learning-/assets/122166125/26e31df3-1977-436a-bbde-8d190a848376)

Random Forest shows better results compared to Logistics Regression

- Gradient Booster

![Screenshot 2023-06-05 154708](https://github.com/Mobisolaa/Detecting-Credit-Card-Frauds-through-Machine-Learning-/assets/122166125/f2a07ae5-5d33-4132-9bab-5a4c8761ff8c)

Gradient Boosting shows worse predictions than the Logistics Regression

###### In conclusion, the Random Forest shows improved predictions compared to the other 2, but with further investigation, data preprocessing feature engineering and exploring other ensemble models, we can arrive at better predictions.
