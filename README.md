# Ireland Housing Affordability Analysis Using Python, Machine Learning and Power BI

## Project Overview

This project analyses housing affordability across Irish counties by combining property price data, earnings data, and population statistics. The main objective is to understand how affordable housing is when average house prices are compared with annual median income.

The project follows a complete data analytics workflow: data cleaning, exploratory data analysis, feature engineering, machine learning, clustering, and dashboard development. Python was used for analysis and modelling, while Power BI was used to create an interactive dashboard for presenting the final insights.

## Business Problem

House prices alone do not fully explain affordability. A county may have high house prices, but it may also have higher income levels. To make the comparison more meaningful, this project uses a price-to-income affordability ratio.

**Affordability Ratio = Average House Price / Annual Income**

A higher ratio means lower housing affordability.

## Key Questions Answered

* Which Irish counties are the least affordable?
* How do average house prices compare with annual income?
* Are higher-income counties always more affordable?
* How are population size and population growth related to house prices?
* Can machine learning help explain county-level house price differences?
* Can counties be grouped into affordability tiers using clustering?

## Tools and Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
* Power BI
* GitHub

## Project Workflow

### 1. Data Cleaning

The raw datasets were cleaned and prepared for analysis. Property prices were converted into numeric format, sale dates were converted into date format, duplicate records were removed, and county names were standardised.

The earnings dataset was cleaned to keep only county-level records. Annual income was calculated from weekly earnings.

### 2. Feature Engineering

New features were created to support the analysis, including:

* Year
* Month
* Annual income
* Population growth
* Average house price
* Affordability ratio
* Affordability tier

### 3. Exploratory Data Analysis

Exploratory analysis was carried out to understand patterns in house prices, income, population, and affordability across Irish counties.

The analysis showed that house prices vary much more strongly between counties than income. This explains why higher-income counties can still face strong affordability pressure.

### 4. Machine Learning

Two regression models were tested:

**Linear Regression**

* R² Score: 0.81
* Mean Absolute Error: €25,607
* Root Mean Squared Error: €31,782

Linear Regression performed well on the county-level dataset and was selected as the stronger model.

**Random Forest**

* R² Score: 0.14
* Mean Absolute Error: €59,399
* Root Mean Squared Error: €67,486

Random Forest performed weaker because the final dataset contained only 26 county-level observations.

### 5. K-Means Clustering

K-Means clustering was used to group counties into three affordability tiers:

| Affordability Tier     | Number of Counties |
| ---------------------- | -----------------: |
| High Affordability     |                 14 |
| Moderate Affordability |                 10 |
| Low Affordability      |                  2 |

Dublin and Wicklow formed the Low Affordability group, showing that the strongest housing pressure is concentrated in a small number of counties.

## Key Findings

* Dublin and Wicklow are the least affordable counties in the analysis.
* Dublin had an affordability ratio of approximately 14.33.
* Wicklow had an affordability ratio of approximately 13.79.
* Kildare, Meath, Galway, Cork, Kilkenny, Wexford, Kerry, and Louth also showed strong affordability pressure.
* Higher-income counties often also have higher average house prices.
* Population size is positively related to average house prices.
* Linear Regression performed better than Random Forest on this small county-level dataset.
* K-Means clustering successfully grouped counties into clear affordability tiers.

## Power BI Dashboard

The Power BI dashboard contains three main pages.

### Executive Overview

This page gives a high-level summary of the housing affordability situation across Irish counties.

![Executive Overview](images/01_executive_overview.png)

### Affordability Analysis

This page focuses on the least affordable counties, income vs house price relationship, and county-level affordability ranking.

![Affordability Analysis](images/02_affordability_analysis.png)

### Cluster Analysis

This page presents the K-Means clustering results and shows how counties are grouped into affordability tiers.

![Cluster Analysis](images/03_cluster_analysis.png)

## Repository Structure

```text
ireland-housing-affordability-analysis/
│
├── data/
│   └── irish_housing_final.csv
│
├── notebooks/
│   └── Housing_Price_Affordability.ipynb
│
├── dashboard/
│   └── Power BI dashboard file
│
├── images/
│   ├── 01_executive_overview.png
│   ├── 02_affordability_analysis.png
│   └── 03_cluster_analysis.png
│
└── README.md
```

## Skills Demonstrated

* Data cleaning
* Exploratory data analysis
* Feature engineering
* Dataset merging
* Regression modelling
* Model evaluation
* K-Means clustering
* Power BI dashboard design
* Data storytelling
* Business insight generation
* GitHub project documentation

## Conclusion

This project provides an end-to-end analysis of housing affordability in Ireland. By combining property prices, earnings, and population data, the analysis identifies counties with the highest housing pressure and explains how affordability varies across Ireland.

The final dashboard makes the results easy to understand and suitable for portfolio presentation, recruiter review, and further analytical development.
