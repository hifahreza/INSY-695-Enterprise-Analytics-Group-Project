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


### Threats to Validity:


### Conclusions:


### Lessons learned and next steps:



