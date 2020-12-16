# Description
The train data was taken from Kaggle and converted to another train and test
with 80%,20% split with SEED of 100 using scikit-learn.

# Dataset Introduction
The dataset is taken from Kaggle competition [Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn) which contains 7043 rows (customers) and 21 columns (features).


The data set includes information about:

- Customers who left within the last month: the column is called `Churn`
- Services that each customer has signed up for: `phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies`
- Customer account information – how long they’ve been a customer, `contract, payment method, paperless billing, monthly charges, and total charges`
- Demographic info about customers – `gender, age range, and if they have partners and dependents`

# Feature Description
| Attribute | Description |
|:-|:-|
| customerId | Customer Id |
| gender | Whether the customer is a male or a female |
| SeniorCitizen | Whether the customer is a senior citizen or not (1, 0) |
| Partner | Whether the customer has a partner or not (Yes, No) |
| Dependents | Whether the customer has dependents or not (Yes, No) |
| tenure | Number of months the customer has stayed with the company |
| PhoneService | Whether the customer has a phone service or not (Yes, No) |
| MultipleLines | Whether the customer has multiple lines or not (Yes, No, No phone service) |
| InternetService | Customer’s internet service provider (DSL, Fiber optic, No) |
| OnlineSecurity | Whether the customer has online security or not (Yes, No, No internet service) |
| OnlineBackup | Whether the customer has online backup or not (Yes, No, No internet service) |
| DeviceProtection | Whether the customer has device protection or not (Yes, No, No internet service) |
| TechSupport | Whether the customer has tech support or not (Yes, No, No internet service) |
| StreamingTV | Whether the customer has streaming TV or not (Yes, No, No internet service) |
| StreamingMovies | Whether the customer has streaming movies or not (Yes, No, No internet service) |
| Contract | The contract term of the customer (Month-to-month, One year, Two year) |
| PaperlessBilling | Whether the customer has paperless billing or not (Yes, No) |
| PaymentMethod | The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic)) |
| MonthlyCharges | The amount charged to the customer monthly |
| TotalCharges | The total amount charged to the customer |
| Churn | Whether the customer churned or not (Yes or No) |

# Notes
- Not churned is 72.4% and churned is 27.6%.
- There are some rows with total charges non-numeric (white space).
- Only three feature names are not CamelCase `customerId, gender, and tenure`. So we can make all of them CamelCase.
