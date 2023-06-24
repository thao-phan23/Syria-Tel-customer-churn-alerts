
![Customer_Churn_Prediction_Models_in_Machine_Learning](https://github.com/thao2023/Phase_3_Project/assets/131706716/137f4e35-2476-41ab-9ae7-c6b2735fa136)
Photo source: https://www.projectpro.io/article/churn-models/709

# Phase_3_Project

## 1. Overview
The telecom industry in the United States is a highly competitive market, where losing customers translates into revenue loss and increased costs. With over 800 operators vying for market share, the industry faces the challenge of a high average churn rate of more than 21%. Acquiring a single customer in this fiercely competitive landscape costs over $300, making customer retention a critical focus for telecom companies. The need to minimize churn and retain customers is paramount in this competitive industry to ensure sustainable growth and profitability.

## 2. Business Understanding:
As one of the players in this fierce industry, Syriatel is actively studying the factors that influence churn rate, emphasizing the importance of identifying key drivers in customer attrition. By uncovering these factors, Syriatel aims to implement effective measures to mitigate churn and enhance customer retention.

### Stakeholder: 

This analysis will provide valuable insights to the top managers, enabling them to make informed decisions and take proactive actions based on factual information about customer behavior prior to churn.

### Key business question: 
What are the alert factors to be aware of before customers leave?

## 3. Data Understanding
### 3.1. Account length:
![Account length](https://github.com/thao2023/Phase_3_Project/assets/131706716/42056944-9f1b-47d7-ba31-b150dc13bfc6)

The churn rate falls between 13% to 16%, which is significantly lower than the average churn rate in the telecom industry, which is approximately 21% (as of 2020). One possible reason that can explain this favorable performance is the promotion of new account registrations.

However, starting from the 3rd month, the churn rate began to rise and remained high in the subsequent months. Based on this observation, the company should take into consideration to start improving retention rates.

### 3.2. International plan & internal call charge:
![intl plan](https://github.com/thao2023/Phase_3_Project/assets/131706716/fbfeb0d1-5712-4699-8949-8c0a6b1d07fe)

![download](https://github.com/thao2023/Phase_3_Project/assets/131706716/08d9263c-b4a1-4b07-ab72-a17f7bc22bfe)

The churn rate of subscribers with an international plan is more than three times higher compared to those without a subscription. In the meantime, As customers pay more for international charges, there is an increased likelihood of them switching to another service provider. This raises concerns that the high cost of international calls might be causing customers to switch to other operators.


### 3.3. Voice mail plan & voice mail messages:
![Voice mail plan](https://github.com/thao2023/Phase_3_Project/assets/131706716/cdb083d8-f54e-4d51-8bce-d0376ab1e17f)

![voice mail messages](https://github.com/thao2023/Phase_3_Project/assets/131706716/85f3fc0e-cd5b-4e03-acbd-639783c1974f)

Accounts with a voicemail plan have a churn rate of approximately 8.6%, whereas accounts without a voicemail plan exhibit a nearly double churn rate of around 16%. On the other hand, churn customers exhibit a lower average number of voicemail messages compared to staying customers.
These observations suggest that customers who actively utilize the company's services are less likely to switch to other operators. Therefore, it is advisable for the company to focus on increasing the number of voicemail subscribers.

### 3.4. Customer service calls:
![cUSTOMER SERVICE CALLS](https://github.com/thao2023/Phase_3_Project/assets/131706716/c46d9424-dc54-4cf5-b80b-a7198ef9b5ec)

After the 3rd customer service call, the churn rate significantly increased from 10.3% to nearly 46%. This observation suggests that customers who encounter numerous service-related issues tend to make multiple calls to customer service before ultimately switching to other service providers.

## 4. Modeling

Utilize 5 different classifiers to build up predictive models:
1. LogisticRegression
2. DecisionTreeClassifier
3. KNeighborsClassifier
4. RandomForestClassifier
5. XGBClassifier

First, running all the models without hyperparameter tuning as the baseline models.
Second, adding hyperparameters to test if the models perform better or not.
Finally, applying the SMOTE technique to the models from the second step to assess if their performance can be enhanced by addressing the imbalanced data's false rate.

## 5. Evaluation

However, the final model that I would like to utilize will be the XGBoost classifier, applying parameter tuning and SMOTE technique as it outperforms others with regard to the levels of accuracy, f1-score, and AUC score.

Another reason that I would prefer the XGBoost classifier is because its performance is more stable than other classifiers even without hyperparameter tuning and SMOTE technique.

The best model confusion matrix and important features are below:

![Confusion matrix](https://github.com/thao2023/Phase_3_Project/assets/131706716/d46d8312-cb98-4e8f-b171-8fa2753e6df6)


![14](https://github.com/thao2023/Phase_3_Project/assets/131706716/33d46e0c-6a54-4b92-9c33-7c28290cb582)

## 6. Conclusion.

Based on the analysis using the XGBoost model, we have identified key alert factors that the company should pay close attention to and take proactive measures. These factors act as early indicators of potential customer churn, enabling the company to intervene and mitigate the associated risks in a timely manner.

Additionally, it provides recommendations based on the findings to improve customer retention and reduce churn rate.
1. Account length: Start a retention plan after 3rd month instead of 6th month to maintain a good churn rate.
2. International plan & international call charge: Conduct a market analysis to compare international call pricing with competitors.
3. Voicemail plan & voicemail messages: Increase voice mail plan subscribers to encourage greater customer engagement with company services.
4. Customer service calls: Set a threshold of customer calls = 3 to pay more attention to these customers to reinforce the retention 
