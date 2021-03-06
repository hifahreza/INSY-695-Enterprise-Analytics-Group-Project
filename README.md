# INSY-695-Enterprise-Analytics-Group-Project

#### Group Members: Michael Church Carson, Hadyan Fahreza, Solomon Gomez, Danyal Hamid, Vahid Hedley, Atrin Morteza Ghasemi, and Reza Soleimani


### Introduction to Use Case: Telecom Customer Churn

![image](https://user-images.githubusercontent.com/93062815/153732516-0a59eab8-3143-46bc-abad-7403ddb0505e.png)

Orange is a French multinational telecommunications company with approximately 266 million customers. Like all telecom companies, one of the constant threats to Orange's business model is customer churn, the rate at which customers leave. In order to protect its top line, Orange cannot just attract new customers, it also needs to minimize the rate at which its current customers are leaving, and likely signing on to a plan with one of its competitors. In that data we have collected about Orange’s customers, the churn rate is approximately 17%. Our objective is to help Orange lower this churn rate. Our industry research suggests that Orange has room for improvement. A recent study of major American telecom/internet providers (AT&T, Verizon, T-Mobile, and Sprint) found that the average rate of churn was approximately 2%. Therefore, we think it is reasonable to reduce Orange's churn rate by 3-5%. To this end, we will analyze the data and develop models that predict churn rate. These models will allow us to identify the factors that are causing customers to leave Orange. 

### Hypothesis:

We hypothesize that there will be two primary predictors of customer churn. First, we think that a high number of calls to Orange's customer service agents will mean that a customer is more likely to Churn. If a customer is calling repeatedly, it is a good indication that they are having trouble with their service and that they are therefore less satisfied with the service and more likely to leave. Secondly, we hypothesize that customers who have large charges will be more likely to leave. If they are paying more, it seems reasonable to think that they will be more critical of Orange's service, possibly less satisfied with it, and more likely to look for alternatives that might be cheaper.

### Data:

The data contains information about the phone plans of 2666 of Orange's customers (see Churn.csv file). The data contains the following columns:

**State** - U.S. state the customer lives in.

**Area_code** - Customer's telephone area code.

**Account_length** - Duration of customers' accounts (months).

**Total_day_minutes** - Total daytime minutes used by the customer.

**Total_day_calls** - Total daytime calls placed by the customer.

**Total_day_charge** - Total daytime charges incurred by the customer.

**Total_eve_minutes** - Total evening minutes used by the customer.

**Total_eve_calls** - Total evening calls placed by the customer.

**Total_eve_charge** - Total evening charges incurred by the customer.

**Total_night_minutes** - Total nighttime minutes used by the customer.

**Total_night_calls** - Total nighttime calls placed by the customer.

**Total_night_charge** - Total nighttime charges incurred by the customer.

**Total_intl_minutes** - Total international minutes used by the customer.

**Total_intl_calls** - Total international calls placed by the customer.

**Total_intl_charge** - Total international charges incurred by the customer.

**International_plan** - Did the customer have an international plan? (Yes or No)

**Voice_mail_plan** - Did the customer have a plan with voicemail? (Yes or No)

**Number_vmail_messages** - Number of voicemail messages used by the customer.

**Customer_service_calls** - Number of calls the customer placed to Orange's customer service center.

**Churn**  - Did the customer leave Orange's plan? (Yes or No)

### Modelling:

To solve this business problem, we ran the following 12 models to better understand the factors that influence the decision by Orange's customers to leave.

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. Gradient Boosting Classifier
5. Light Gradient Boosting Machine Classifier
6. Extreme Gradient Boosting Classifier
7. Support Vector Classifier
8. AdaBoost
9. TPOTClassifier
10. CatBoostClassifier
11. ANN - Sequential Model
12. Causal Inference

### Results:

The models are optimized for recall as the inability to identify prospective customers who would actually churn would lead to missed revenue generation opportunity. Thus, minimizing the false negative rate is the foremost priority in developing the model.

Two best performing models out of 12 models mentioned above:

1. CatBoost: 91% recall in predicting churn of customers
2. AdaBoost: 81% recall in predicting churn of customers

#### Feature Importance:

Most important features based on CatBoost model:
1. Total minutes
2. Customer service calls
3. Voicemail feature
4. Total day charges

Most important features based on AdaBoost model:
1. Customer service calls
2. Total minutes
3. Total calls
4. Area codes

#### Causal Inference:

Treatment: Customer Service Calls (most important feature in AdaBoost model)

Package: CausalML

Binary Approach:
1. No Service Calls: 13.92% Churn
2. Any Service Calls: 14.95% Churn

Bucketed Approach:
1. No Service Calls: 13.89% Churn
2. 1-3 Service Calls: 10.24% Churn
3. 4-9 Service Calls: 55.74% Churn

Insight: A customer making 1-3 service calls is not an issue, but making 4-9 service calls greatly increases the risk of churn.

### Threats to Validity:

Although our model is already having a very satisfactory accuracy, precision, and recall, our model is still subjected to prediction errors. The Adaboost model has an AUC score of 0.88, 8 false negatives and 32 false positives. Meanwhile the Catboost model has an AUC score of 0.92, 5 false negatives and 32 false positives out of 320 observations. This shows that our model is still subjected to a certain degree of uncertainty.

### Recommendations:

1. Orange should invest in customer service:
   - Orange should improve the quality of its customer service
   - Ensure that customers do not have to call back more than 3 times. The rate of attrition increases significantly when customers have to call back several times.

2. Customers who do not have voicemail are more likely to churn
   - Orange should offer voicemail as a standard feature. 

3. Customers who have a lot of minutes are more likely to churn.
   - Orange should offer a reduced rate per minute after customers pass a certain number of total calling minutes. 


### Lessons learned and next steps:

It is insufficient for telecom companies to focus on their product alone. They must also pay attention to the service they are providing. Our analysis shows that the single greatest predictor of churn is the number of customer service calls a customer makes. Granted, one could argue that people are calling because of some other issue and that it is this issue that leads them to churn. However, we found that the more times someone calls, the more likely they are to leave, especially if they call more than 3 times. Therefore, it seems that the calls themselves are leading people to leave.

We also learnt that customers are price elastic. That is, their demand is affected by the price of their plan. The customers who have more minutes, and consequently pay more, are more likely to churn. This is why we recommended that Orange begin a program that decreases the price per minute of calling for customers who have high monthly minutes. Receiving less money per minute once the customer passes a certain usage threshold is better than losing their business altogether.

Overall, we learnt that customer churn can be primarily explained by a few factors: number of service calls, inclusion of voicemail feature, and number of minutes used. This means that there is strong potential for Orange to improve their churn rate by creating policies that focus on these key determinants of churn. Admittedly, our sample of customers was not that large, and it was focused on three regions in California. Thus, in the future, we would recommend that Orange replicate our analysis with a larger sample of customers so that they can design policies which limit preventable churn. There will always be some percentage of customers who will leave their plan, but our analysis shows that it is possible to identify why customers are leaving and to design policies to prevent them from doing so.



