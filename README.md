# 📊 Telco Customer Churn Analysis & Retention Strategy

## 📌 Project Overview

Customer churn is one of the major challenges faced by telecommunication companies. Losing existing customers can directly affect revenue and long-term business growth.

This project analyzes customer data from a telecommunications company to identify the key factors influencing customer churn. The analysis focuses on customer demographics, tenure, contract type, internet services, payment methods, monthly charges, total charges, and value-added services.

The project uses **Exploratory Data Analysis (EDA), Data Visualization, Feature Engineering, and Correlation Analysis** to understand customer behavior and generate actionable business recommendations for improving customer retention.

---

## 🎯 Project Objectives

* Analyze the overall customer churn pattern.
* Identify the major factors influencing customer churn.
* Understand the relationship between customer tenure and churn.
* Analyze churn across different contract types.
* Study the impact of monthly and total charges.
* Analyze churn based on payment methods and internet services.
* Understand the impact of Tech Support and Online Security.
* Identify high-risk customer segments.
* Generate business recommendations to improve customer retention.

---

## 📂 Dataset

The dataset contains customer-level information from a telecommunications company.

### Dataset Size

* **Rows:** 7,043 customers
* **Columns:** 21
* **Target Variable:** `Churn`

### Dataset Features

| Feature            | Description                                               |
| ------------------ | --------------------------------------------------------- |
| `customerID`       | Unique customer identifier                                |
| `gender`           | Customer gender                                           |
| `SeniorCitizen`    | Indicates whether the customer is a senior citizen        |
| `Partner`          | Whether the customer has a partner                        |
| `Dependents`       | Whether the customer has dependents                       |
| `tenure`           | Number of months the customer has stayed with the company |
| `PhoneService`     | Whether phone service is subscribed                       |
| `MultipleLines`    | Multiple phone lines subscription                         |
| `InternetService`  | Type of internet service                                  |
| `OnlineSecurity`   | Online security subscription                              |
| `OnlineBackup`     | Online backup subscription                                |
| `DeviceProtection` | Device protection subscription                            |
| `TechSupport`      | Technical support subscription                            |
| `StreamingTV`      | Streaming TV subscription                                 |
| `StreamingMovies`  | Streaming movies subscription                             |
| `Contract`         | Contract duration                                         |
| `PaperlessBilling` | Paperless billing preference                              |
| `PaymentMethod`    | Customer payment method                                   |
| `MonthlyCharges`   | Monthly amount charged                                    |
| `TotalCharges`     | Total amount charged                                      |
| `Churn`            | Whether the customer left the company                     |

---

## 🛠️ Tools & Technologies

### Programming Language

* Python

### Libraries Used

* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization and correlation heatmap
* **Plotly Express** – Interactive visualizations
* **Scikit-learn** – Data preprocessing and Label Encoding
* **Warnings** – Warning management

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
Unique Value Analysis
   ↓
Exploratory Data Analysis
   ↓
Data Visualization
   ↓
Outlier Detection
   ↓
Feature Engineering
   ↓
Categorical Encoding
   ↓
Correlation Analysis
   ↓
Business Insights
   ↓
Retention Recommendations
```

---

# 🔍 Data Understanding

The dataset was initially explored using:

* `head()`
* `tail()`
* `info()`
* `shape`
* `columns`
* `describe()`
* `describe(include='object')`
* `isnull().sum()`
* `nunique()`
* `unique()`

These operations helped understand the dataset structure, feature types, unique categories, missing values, and numerical distributions.

---

# 🧹 Data Cleaning & Preprocessing

The following preprocessing activities were performed:

### Missing Value Check

Missing values were checked using:

```python
df.isnull().sum()
```

The `TotalCharges` column was also specifically checked for blank values.

### Categorical Encoding

Categorical variables were converted into numerical form using **LabelEncoder**.

Features encoded included:

* Gender
* Partner
* Dependents
* PhoneService
* MultipleLines
* InternetService
* OnlineSecurity
* OnlineBackup
* DeviceProtection
* TechSupport
* StreamingTV
* StreamingMovies
* Contract
* PaperlessBilling
* PaymentMethod
* Churn

---

# 📈 Exploratory Data Analysis & Visualization

EDA was performed to understand customer behavior and identify patterns associated with churn.

---

## 1. Overall Churn Distribution

### Visualization

A donut/pie chart was used to compare customers who stayed with the company against customers who churned.

### Key Findings

* The majority of customers remain with the company.
* A considerable proportion of customers have churned.
* Churn represents potential revenue loss for the company.
* Customer retention is therefore an important business priority.

### Business Insight

The company should focus on identifying high-risk customers early and provide targeted retention strategies before they leave.

---

## 2. Churn by Gender

### Visualization

A grouped histogram was used to compare churn across male and female customers.

### Key Findings

* Male and female customers show similar churn patterns.
* Gender does not appear to be a major driver of churn.
* There is no significant difference in churn behavior based only on gender.

### Business Insight

Gender-specific retention campaigns may not provide significant benefits. The company should instead focus on behavioral, billing, contract, and service-related factors.

---

## 3. Churn by Senior Citizen Status

### Key Findings

* Senior citizens show a comparatively higher churn tendency.
* Non-senior customers represent the majority of the customer base.
* Senior customers may require additional assistance.

### Business Insight

The company could provide:

* Personalized customer support
* Simplified service plans
* Loyalty benefits
* Dedicated assistance

to improve retention among senior customers.

---

## 4. Churn by Contract Type

### Key Findings

* **Month-to-month customers have the highest churn.**
* One-year contract customers show lower churn.
* Two-year contract customers show the lowest churn.
* Longer contracts are associated with stronger customer loyalty.

### Business Insight

The company should encourage customers to move from month-to-month contracts to longer-term contracts using:

* Annual subscription discounts
* Loyalty rewards
* Contract upgrade offers
* Additional service benefits

Long-term contracts can improve both retention and revenue stability.

---

## 5. Churn by Internet Service Type

### Key Findings

* Fiber optic customers show higher churn compared with DSL customers.
* DSL customers generally demonstrate better retention.
* Customers without internet service show very low churn.

### Business Insight

The company should investigate:

* Fiber pricing
* Network/service quality
* Customer satisfaction
* Technical issues
* Competitor pricing

for fiber optic customers.

---

## 6. Churn by Payment Method

### Key Findings

* Customers using **Electronic Check** show the highest churn.
* Customers using automatic payment methods generally show better retention.
* Bank transfer and credit card users appear relatively more loyal.

### Business Insight

The company can encourage automatic payment enrollment through:

* Auto-pay discounts
* Promotional offers
* Convenient payment options
* Customer education

The reason behind the high churn among electronic check users should also be investigated.

---

## 7. Tenure Distribution by Churn

### Key Findings

* Customers with short tenure are significantly more likely to churn.
* Long-term customers are less likely to leave.
* Customer loyalty increases as tenure increases.

### Business Insight

The **early customer lifecycle is a critical retention period**.

The company should introduce:

* New customer onboarding
* Early engagement campaigns
* Welcome offers
* First-month support
* Personalized communication

to reduce early-stage churn.

---

## 8. Monthly Charges Density by Churn

### Key Findings

* Customers with higher monthly charges tend to churn more frequently.
* Lower monthly charges are associated with better retention.
* Pricing may influence customer churn decisions.

### Business Insight

The company should review high-priced plans and consider:

* Discounts
* Bundled services
* Flexible plans
* Loyalty pricing
* Value-added benefits

for high-paying customers.

---

## 9. Total Charges vs Tenure

### Visualization

A scatter plot was used to study the relationship between `tenure` and `TotalCharges`.

### Key Findings

* Total charges increase as customer tenure increases.
* Long-term customers contribute more lifetime revenue.
* Churned customers are concentrated more heavily among lower-tenure customers.

### Business Insight

Increasing customer lifetime can significantly increase Customer Lifetime Value (CLV).

Therefore, preventing early churn can have a strong positive impact on long-term revenue.

---

## 10. Churn by Tech Support

### Key Findings

* Customers without Tech Support show higher churn.
* Customers receiving technical support demonstrate better retention.
* Technical assistance can improve customer satisfaction.

### Business Insight

The company should:

* Promote Tech Support packages.
* Include Tech Support in premium plans.
* Provide proactive technical assistance.
* Offer support benefits to high-risk customers.

---

## 11. Churn by Online Security

### Key Findings

* Customers without Online Security show higher churn.
* Customers with Online Security demonstrate better retention.
* Security services can increase customer confidence.

### Business Insight

Online Security can be promoted as part of bundled internet packages.

The company can offer security features during onboarding and encourage existing customers to activate them.

---

## 12. Churn by Paperless Billing

### Key Findings

* Paperless billing customers show comparatively higher churn.
* Traditional billing customers appear slightly more stable.
* Paperless billing alone should not be treated as a direct cause of churn.

### Business Insight

Paperless billing should be analyzed together with other variables such as:

* Contract type
* Payment method
* Tenure
* Monthly charges

This can help identify the actual high-risk customer segments.

---

## 13. Average Monthly Charges by Contract & Churn

### Key Findings

* Churned customers often have higher average monthly charges.
* Month-to-month customers have relatively higher charges and higher churn.
* Two-year contract customers generally have lower average charges and lower churn.

### Business Insight

A combination of **high monthly charges + month-to-month contract** represents an important churn-risk segment.

The company should consider:

* Long-term contract discounts
* Loyalty rewards
* Customized pricing
* Premium service bundles

for these customers.

---

# 📦 Outlier Detection

Boxplots were used to inspect numerical features for potential outliers.

### Key Findings

* No major abnormal outliers were identified across most features.
* `tenure` has a wide distribution because customers include both new and long-term subscribers.
* `MonthlyCharges` shows moderate variability.
* `TotalCharges` generally increases with tenure.
* Binary service features naturally contain concentrated values.
* `SeniorCitizen` is highly skewed because senior customers represent a smaller portion of the dataset.

Overall, the dataset was considered suitable for further analysis without extensive outlier treatment.

---

# 🔗 Feature Relationship Analysis

A correlation heatmap was created using Seaborn to understand relationships between numerical/encoded features.

### Important Relationships

### Tenure ↔ TotalCharges

A strong positive relationship exists between tenure and total charges.

**Interpretation:**
Customers who stay longer naturally accumulate higher total charges.

### Tenure ↔ Churn

Tenure has a negative relationship with churn.

**Interpretation:**
Customers with longer tenure are less likely to leave.

### MonthlyCharges ↔ Churn

Monthly charges show a positive relationship with churn.

**Interpretation:**
Customers paying higher monthly amounts show a greater tendency to churn.

### MonthlyCharges ↔ TotalCharges

There is a positive relationship between monthly charges and total charges.

**Interpretation:**
Customers with higher monthly plans generally accumulate greater total charges over time.

### SeniorCitizen ↔ Churn

The relationship is relatively weak.

**Interpretation:**
Age alone is not a strong explanation for customer churn.

---

# 📌 Key Business Findings

The analysis identified several important churn drivers:

1. **Short-tenure customers are more likely to churn.**
2. **Month-to-month customers have the highest churn tendency.**
3. **Higher monthly charges are associated with higher churn.**
4. **Fiber optic customers show higher churn patterns.**
5. **Electronic Check users show higher churn.**
6. **Customers without Tech Support are more likely to churn.**
7. **Customers without Online Security show higher churn.**
8. **Long-term customers are considerably more loyal.**
9. **Total Charges are strongly influenced by tenure.**
10. **Gender has little influence on churn compared with behavioral factors.**

---

# 🎯 High-Risk Customer Profile

Based on the EDA findings, a customer with the following characteristics can be considered a potentially high-risk churn customer:

```text
Short Tenure
     +
Month-to-Month Contract
     +
High Monthly Charges
     +
Fiber Optic Internet
     +
Electronic Check Payment
     +
No Tech Support
     +
No Online Security
     ↓
Higher Churn Risk
```

This customer segment should receive proactive retention attention.

---

# 💡 Business Recommendations

### 1. Improve New Customer Onboarding

The first few months are critical.

Introduce:

* Welcome programs
* Dedicated support
* Early engagement campaigns
* Personalized offers

---

### 2. Promote Long-Term Contracts

Encourage month-to-month customers to move toward one-year or two-year contracts.

Possible strategies:

* Contract discounts
* Loyalty rewards
* Free service upgrades
* Additional benefits

---

### 3. Review High Monthly Charges

High-paying customers should receive additional value.

Possible strategies:

* Customized plans
* Discounts
* Bundled services
* Loyalty pricing

---

### 4. Encourage Automatic Payments

Electronic Check users show higher churn.

Encourage customers to switch to automatic payment methods using incentives and discounts.

---

### 5. Strengthen Customer Support

Customers without Tech Support have higher churn.

Offer technical assistance as part of premium or bundled packages.

---

### 6. Promote Online Security

Online Security users demonstrate better retention.

Bundle security services with internet plans and highlight their benefits during onboarding.

---

### 7. Monitor Fiber Optic Customers

Since fiber customers show higher churn, the company should investigate:

* Pricing
* Service quality
* Network reliability
* Customer complaints
* Competitor offerings

---

### 8. Build a Churn-Risk Monitoring System

Customer behavior can be continuously monitored to identify high-risk customers.

Potential risk indicators include:

* Low tenure
* High monthly charges
* Month-to-month contract
* Electronic Check payment
* Lack of Tech Support
* Lack of Online Security

---

# 📊 Technologies Used

```text
Python
│
├── Pandas
├── NumPy
├── Matplotlib
├── Seaborn
├── Plotly
└── Scikit-learn
```

---

# 📁 Project Structure

```text
Telco-Customer-Churn/
│
├── Telecom_Customer_Churn_Analysis_&_Retention_Strategy.ipynb
├── Telco-Customer-Churn.csv
├── README.md
└── images/
    └── visualizations/
```

---

# 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn
```

### 3. Open the Notebook

```bash
jupyter notebook
```

Open:

```text
Telecom_Customer_Churn_Analysis_&_Retention_Strategy.ipynb
```

### 4. Run the Notebook

Execute the cells sequentially to reproduce the analysis and visualizations.

---

# 📌 Conclusion

The Telco Customer Churn analysis shows that **customer tenure, contract type, monthly charges, payment method, internet service, and value-added services** are important factors associated with customer churn.

Customers with **short tenure, month-to-month contracts, higher monthly charges, electronic check payments, and limited access to services such as Tech Support and Online Security** represent important retention-risk segments.

The analysis highlights that customer retention should focus particularly on the **early stages of the customer lifecycle**, while long-term contracts, personalized pricing, proactive support, and value-added services can help improve customer loyalty.

Overall, the project demonstrates how **data analysis and visualization can convert customer data into actionable business strategies for reducing churn and improving long-term customer value.**

---
