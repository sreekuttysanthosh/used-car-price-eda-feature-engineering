# Used Car Price — EDA & Feature Engineering

## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA), data cleaning, and basic Feature Engineering on a messy used-car dataset.

The main objective is to understand how factors such as car age, kilometers driven, engine capacity, and number of previous owners are associated with the resale price of a used car.

This project was completed as part of an ML internship to practice the fundamentals of preparing real-world-style data for machine learning.

---

##  Problem Statement

Analyze used-car characteristics to understand the factors associated with resale price and prepare the dataset for basic machine learning.

**Target Variable:** `price_lakh`

---

##  Dataset

The dataset contains information about used cars with the following variables:

| Feature | Description |
|---|---|
| `car_age_years` | Age of the car in years |
| `km_driven` | Total kilometers driven |
| `engine_cc` | Engine capacity in CC |
| `owners` | Number of previous owners |
| `price_lakh` | Resale price in lakh |

The dataset intentionally contains common data-quality issues such as missing values, duplicate records, invalid values, and outliers.

---

##  Exploratory Data Analysis

The following EDA steps were performed:

- Dataset shape and structure inspection
- Column and data-type inspection
- Summary statistics
- Missing-value analysis
- Duplicate-row detection
- Invalid-value investigation
- Outlier detection using boxplots
- Distribution analysis using histograms
- Feature vs target analysis
- Correlation analysis using a heatmap

### Relationships Analyzed

- Car age vs price
- Kilometers driven vs price
- Engine capacity vs price
- Number of owners vs price

---

##  Data Cleaning

The dataset was checked and cleaned for:

- Duplicate rows
- Missing values
- Negative car age
- Negative kilometers driven
- Unrealistic owner counts
- Invalid values affecting analysis

After cleaning, the dataset was re-checked to ensure that the data was suitable for further analysis and feature engineering.

---

##  Feature Engineering

Two additional features were created:

### 1. `km_per_year`

Represents the average kilometers driven per year.
```text
km_per_year = km_driven / car_age_years 
```
This provides an additional measure of vehicle usage relative to the number of previous owners.

##  2. km_per_owner 
```text
km_per_owner = km_driven / owners
```
This provides an additional measure of vehicle usage relative to the number of previous owners.


## Key observations 

The EDA was used to examine how vehicle characteristics relate to resale price.

Some important patterns observed include:

* Car age shows a negative relationship with resale price.
* Higher kilometers driven generally tend to be associated with lower resale prices.
* Engine capacity shows a positive association with price in the dataset.
* The number of previous owners has a weaker relationship with price compared with some of the other numerical features.
* Outlier analysis helped identify unusually high or low values that could affect statistical analysis.

These observations are based on the dataset used in this project and do not necessarily represent the entire used-car market.


## Tool & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook 


## Project Structure

```text
used-car-price-eda-feature-engineering/
│
├── data/
│   └── 09_used_car_price.csv
│
├── notebooks/
│   └── Beginner EDA + Feature Engineering.ipynb
│
└── README.md
```

## How to run

1. Clone the repository.
2. Open the project in VS Code or Jupyter Notebook.
3. Open:
notebooks/Beginner EDA + Feature Engineering.ipynb
4. Make sure the dataset path points to:
data/09_used_car_price.csv
5. Run the notebook cells sequentially.


## Learning Outcomes
Through this project, I practiced:
* Loading datasets using Pandas
* Understanding dataset structure
* Checking data quality
* Handling missing values
* Detecting duplicate records
* Identifying invalid values
* Detecting outliers
* Creating data visualizations
* Understanding feature-target relationships
* Using correlation analysis
* Performing basic feature engineering
* Separating features (X) and target (y)
* Preparing data for basic machine learning

## Author
Sreekutty Santhosh