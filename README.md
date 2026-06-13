# Ireland Housing Affordability Analysis Using Python, Machine Learning and Power BI

## Project Overview

This project analyses housing affordability across Irish counties by combining property price data, county-level earnings data, and population statistics. The main objective is to understand how affordable housing is when average house prices are compared with annual median income.

The project follows a complete data analytics workflow, including data cleaning, exploratory data analysis, feature engineering, machine learning, clustering, and dashboard development. Python was used for analysis and modelling, while Power BI was used to create an interactive dashboard for presenting the final insights.

This project was created to answer a real-world question: **which Irish counties are under the strongest housing affordability pressure, and how does income compare with average house prices?**

---

## Business Problem

House prices alone do not fully explain affordability. A county may have high average house prices, but it may also have higher income levels. Similarly, a county may have lower house prices but still be difficult to afford if income levels are also low.

To make the comparison more meaningful, this project uses a price-to-income affordability ratio:

**Affordability Ratio = Average House Price / Annual Income**

A higher affordability ratio means lower housing affordability. This ratio helps compare counties more fairly by looking at both house prices and income together.

---

## Key Questions Answered

This project answers the following questions:

* Which Irish counties are the least affordable?
* How do average house prices compare with annual income?
* Are higher-income counties always more affordable?
* How are population size and population growth related to house prices?
* Can machine learning help explain county-level house price differences?
* Can counties be grouped into affordability tiers using clustering?
* How can these findings be presented clearly using Power BI?

---

## Data Sources

The project uses three main datasets:

1. **Irish Property Price Register Data**
   Used to calculate recent average house prices by county.

2. **County-Level Earnings Data**
   Used to estimate annual income by county.

3. **Population Data**
   Used to analyse population size, population growth, and regional demand pressure.

The final merged dataset contains 26 Irish counties with house price, income, population, affordability, and clustering information.

## Data Notes

The repository includes the final cleaned county-level dataset used for analysis and dashboard development.

The full raw Property Price Register file was not uploaded because it is a large transaction-level dataset. Instead, the project notebook shows the cleaning and aggregation process used to create county-level average house prices.

Raw data sources used in this project include:

- Irish Property Price Register
- CSO county-level earnings data
- CSO population data

---

## Tools and Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
* Power BI
* GitHub

---

## Project Workflow

### 1. Data Cleaning

The raw datasets were cleaned and prepared before analysis. Property prices were converted into numeric format, sale dates were converted into date format, duplicate records were removed, and county names were standardised.

The earnings dataset also required cleaning because the original Excel file had a complex structure. The national total row was removed so that only county-level records were included in the final analysis.

Population data was cleaned and used to create a new population growth feature.

---

### 2. Feature Engineering

Several new variables were created to support the analysis:

* Year
* Month
* Annual income
* Population growth
* Average house price
* Affordability ratio
* Affordability tier

The affordability ratio became the main measure used to compare counties.

---

### 3. Exploratory Data Analysis

Exploratory data analysis was carried out to understand patterns in house prices, income, population, and affordability across Irish counties.

The analysis showed that house prices vary much more strongly between counties than income. This is an important finding because it explains why some higher-income counties can still face strong affordability pressure.

---

### 4. Machine Learning

Two regression models were tested to understand whether income and population-related features could explain county-level house prices.

#### Linear Regression

Linear Regression performed well on the county-level dataset.

| Metric                  |  Result |
| ----------------------- | ------: |
| R² Score                |    0.81 |
| Mean Absolute Error     | €25,607 |
| Root Mean Squared Error | €31,782 |

Linear Regression was selected as the stronger model because it performed better and was more suitable for the small county-level dataset.

#### Random Forest

Random Forest was used as a comparison model.

| Metric                  |  Result |
| ----------------------- | ------: |
| R² Score                |    0.14 |
| Mean Absolute Error     | €59,399 |
| Root Mean Squared Error | €67,486 |

Random Forest performed weaker because the final dataset contained only 26 county-level observations. This shows that simpler models can sometimes perform better when the dataset is small.

---

### 5. K-Means Clustering

K-Means clustering was used to group counties into three affordability tiers:

* High Affordability
* Moderate Affordability
* Low Affordability

| Affordability Tier     | Number of Counties |
| ---------------------- | -----------------: |
| High Affordability     |                 14 |
| Moderate Affordability |                 10 |
| Low Affordability      |                  2 |

Dublin and Wicklow formed the Low Affordability group, showing that the strongest housing pressure is concentrated in a small number of counties.

---

## Key Findings

The main findings from the project are:

* Dublin and Wicklow are the least affordable counties in the analysis.
* Dublin had an affordability ratio of approximately 14.33.
* Wicklow had an affordability ratio of approximately 13.79.
* Kildare, Meath, Galway, Cork, Kilkenny, Wexford, Kerry, and Louth also showed strong affordability pressure.
* Higher-income counties often also have higher average house prices.
* Population size is positively related to average house prices.
* Linear Regression performed better than Random Forest on this small county-level dataset.
* K-Means clustering successfully grouped counties into clear affordability tiers.
* Power BI helped convert the analysis into clear and interactive dashboard insights.

---

## Power BI Dashboard

The Power BI dashboard contains three main pages.

### Executive Overview

This page gives a high-level summary of the housing affordability situation across Irish counties. It includes KPI cards, an affordability ratio ranking by county, and a slicer for affordability tiers.

![Executive Overview](./images/Ireland%20Housing%20Affordability%20Analysis.png)

---

### Affordability Analysis

This page focuses on the least affordable counties, the relationship between annual income and average house prices, and county-level affordability ranking.

![Affordability Analysis](./images/Affordability%20Analysis.png)

---

### Cluster Analysis

This page presents the K-Means clustering results and shows how counties are grouped into affordability tiers.

![Cluster Analysis](./images/Cluster%20Analysis.png)

---

## Dashboard Insights

The dashboard shows that Dublin and Wicklow have the strongest affordability pressure. Dublin has the highest affordability ratio, meaning the average house price is more than 14 times annual median income.

The cluster analysis also shows that only two counties fall into the Low Affordability group, but these counties have much higher average house prices compared with the other groups. This suggests that the affordability problem is strongly concentrated in a small number of high-pressure counties.

---

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
│   ├── Ireland Housing Affordability Analysis.png
│   ├── Affordability Analysis.png
│   └── Cluster Analysis.png
│
├── report/
│   └── Ireland_Housing_Affordability_Professional_Report.docx
│
└── README.md
---

## Skills Demonstrated

This project demonstrates the following skills:

* Data cleaning
* Data preprocessing
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

---

## Conclusion

This project provides an end-to-end analysis of housing affordability in Ireland. By combining property prices, earnings, and population data, the analysis identifies counties with the highest housing pressure and explains how affordability varies across Ireland.

The results show that Dublin and Wicklow are the least affordable counties, while most counties fall into High or Moderate Affordability groups. Machine learning helped explain house price differences, and clustering provided a clear way to group counties based on affordability pressure.
