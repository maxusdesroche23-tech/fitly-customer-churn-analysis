# Fitly Customer Churn Analysis

## Project Overview

Customer retention is a major challenge for subscription-based businesses. This project analyzes customer behavior at **Fitly**, a fitness subscription platform, to identify engagement patterns, support trends, subscription characteristics, and limitations in the available churn data.

The analysis combines information from three data sources:

- Customer account and subscription information
- Customer support interactions
- User activity and engagement records

The project demonstrates data validation, cleaning, transformation, exploratory data analysis, visualization, and business-focused communication using Python.

## Business Questions

This analysis addresses the following questions:

1. What does the available churn information show?
2. How are customers distributed across subscription plans?
3. How does customer engagement vary across the user base?
4. What patterns appear in customer support activity?
5. Which metrics should Fitly monitor to improve customer retention?

## Dataset Overview

| Dataset | Description |
|---|---|
| Account Information | Customer profile, location, subscription plan, and available churn status |
| Customer Support | Support tickets, communication channels, issue topics, and resolution time |
| User Activity | Customer activity and engagement events |

The analysis covers:

- **400 customers**
- **445 activity records**
- **918 support records**

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Data Preparation

The data-cleaning and preparation process included:

- Inspecting dataset dimensions and data types
- Identifying missing values
- Detecting duplicate records
- Standardizing email addresses
- Standardizing categorical variables
- Converting timestamps to datetime format
- Creating numeric customer identifiers
- Converting available churn labels into binary values
- Aggregating activity and support metrics by customer
- Combining the datasets for customer-level analysis

## Exploratory Data Analysis

The exploratory analysis focuses on:

- Available churn information
- Subscription-plan distribution
- Customer activity and engagement
- Customer-support interactions
- Relationships between operational metrics
- Data-quality limitations

## Key Findings

### 1. Churn data is incomplete

Only **114 of 400 customers** have a recorded churn status.

Churn information is missing for **286 customers**, representing **71.5%** of the customer base.

Every customer with a recorded status is classified as churned. Therefore, the observed 100% churn rate among those records does not represent Fitly's true company-wide churn rate.

### 2. Retained customers cannot be identified

The available data contains no customers explicitly classified as retained.

This prevents reliable comparisons between churned and retained customers. The analysis cannot establish whether engagement, subscription plan, or support activity causes or predicts churn.

### 3. Engagement varies across customers

Customer activity differs across the user base and subscription plans.

These differences can help Fitly identify low-engagement customer segments. However, incomplete churn labels prevent the analysis from confirming whether lower engagement is associated with customer cancellation.

### 4. Support activity is an important operational metric

Across the complete customer dataset, customers generated approximately:

- **2.29 support tickets per customer**
- **10.23 hours of average resolution time**

Ticket volume, recurring issues, and resolution time should be monitored as potential indicators of customer dissatisfaction.

## Recommendations

### Improve churn-status tracking

Fitly should record a complete and consistent churn status for every customer.

### Identify retained customers

Active and retained customers should be clearly classified to enable valid comparisons with churned customers.

### Monitor customer engagement

Fitly should track activity frequency and identify customers whose engagement is declining.

### Improve support efficiency

The company should monitor ticket volume, recurring support issues, and resolution time.

### Develop a retention dashboard

A retention dashboard could track:

- Churn status
- Customer activity
- Subscription plans
- Support-ticket volume
- Resolution time
- Customer retention outcomes

### Reevaluate churn drivers

Once complete churn data becomes available, Fitly should compare churned and retained customers and consider developing a predictive churn model.

## Data Limitations

The primary limitation of this project is the incomplete churn information.

Because 71.5% of customers have no recorded churn status and the remaining customers are all classified as churned, the dataset cannot currently support:

- A reliable company-wide churn rate
- Valid comparisons between churned and retained customers
- Causal conclusions about churn drivers
- A dependable churn-prediction model

The current findings should therefore be interpreted as descriptive insights rather than confirmed churn relationships.

## Repository Structure

```text
fitly-customer-churn-analysis/
├── README.md
├── Fitly_Customer_Churn_Analysis.ipynb
├── requirements.txt
└── Data/
    ├── da_fitly_account_info.csv
    ├── da_fitly_customer_support.csv
    └── da_fitly_user_activity.csv
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/maxusdesroche23-tech/fitly-customer-churn-analysis.git
cd fitly-customer-churn-analysis
```

### 2. Install the required libraries

```bash
pip install -r requirements.txt
```

Alternatively, install the libraries directly:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Start Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open the notebook

Open the following file:

```text
Fitly_Customer_Churn_Analysis.ipynb
```

Run the notebook cells in order from top to bottom.

## Future Improvements

Future versions of this project could include:

- Complete churn and retention labels
- Customer tenure information
- Payment and billing history
- Monthly engagement trends
- Customer lifetime value
- Statistical hypothesis testing
- Customer segmentation
- Machine-learning churn prediction
- An interactive retention dashboard

## Author

**Max Desroches**

Aspiring Data Analyst with experience in Python, SQL, data cleaning, exploratory data analysis, data visualization, and business-focused reporting.
