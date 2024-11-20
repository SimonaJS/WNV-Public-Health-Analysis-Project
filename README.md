# West Nile Virus (WNV) Analysis: A Data-Driven Approach to Public Health Surveillance

## Overview
This repository contains the code and resources for analyzing mosquito tracking data from Chicago, Illinois, to better understand the spread of West Nile Virus (WNV). The project is divided into two deliverables that cover data wrangling, exploratory data analysis (EDA), and advanced statistical modeling. The objective is to analyze trends in mosquito populations and WNV prevalence to support public health efforts.

## Problem Statement
West Nile Virus (WNV) is a mosquito-borne disease that poses a significant health risk to urban populations. By analyzing mosquito tracking data collected between 2008 and 2019, this project aims to uncover patterns and insights that can inform disease surveillance and prevention strategies.

## Impact
The findings of this project can have the following impacts:
- **Improved Public Health Surveillance**: Providing actionable insights into mosquito populations and WNV prevalence to help authorities focus prevention efforts.
- **Disease Prevention**: Identifying patterns in mosquito species and WNV spread to mitigate risks.
- **Data-Driven Decisions**: Enhancing urban planning and public health strategies based on data insights.

---

## Deliverable 1: Data Wrangling and Exploratory Data Analysis (EDA)

### Objective
The first deliverable focuses on cleaning and understanding the data using basic and advanced EDA techniques to identify relationships between variables and uncover trends in mosquito populations and WNV prevalence.

### The Dataset
The dataset includes mosquito tracking data collected from traps across Chicago.

| **Column Name**         | **Description**                                                | **Data Type** | **Notes**                                                                                              |
|--------------------------|----------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------|
| Year                    | Year that the WNV test is performed                            | int64         |                                                                                                        |
| Week                    | Week that the WNV test is performed                            | int64         |                                                                                                        |
| Address Block           | Address of the location of trap                                | string        |                                                                                                        |
| Block                   | Block number of address                                        | int64         |                                                                                                        |
| Trap                    | ID of the trap                                                | string        | Some traps are "satellite traps" set up within 6 blocks of an established trap to enhance surveillance. |
| Trap Type               | Type of trap                                                  | string        |                                                                                                        |
| Date                    | Date and time of the WNV test                                 | string        | Records exist only when a mosquito species is found at a trap.                                         |
| Mosquito Number         | Number of mosquitoes caught                                   | int64         | Counts exceeding 50 are split into multiple rows.                                                     |
| Mosquito ID             | ID for mosquito species                                       | string        |                                                                                                        |
| WNV Present             | Presence of WNV in mosquitoes                                 | string        |                                                                                                        |
| Species                 | Mosquito species                                              | string        |                                                                                                        |
| Lat                     | Latitude of trap                                              | float64       |                                                                                                        |
| Lon                     | Longitude of trap                                             | float64       |                                                                                                        |

### Key Tasks
- **Data Wrangling**:
  - Convert the `Date` column to datetime format.
  - Identify and address null values.
  - Remove duplicate or redundant columns.
- **Basic EDA**:
  - Analyze the distributions of numeric and categorical variables.
  - Visualize the relationship between mosquito number and date.
- **Advanced EDA**:
  - Explore relationships between mosquito species and WNV prevalence.
  - Investigate the relationship between trap type and mosquito numbers.
  - Generate additional insights through innovative visualizations.

---

## Deliverable 2: Statistical and Advanced Data Analysis

### Objective
The second deliverable expands on the EDA findings with advanced statistical and machine learning analyses to study the relationships between mosquito species, WNV presence, and environmental factors.

### Key Tasks

#### **Part 1: Basic Analysis**
- Convert `WNV Present` to a binary column.
- Create dummy variables for `Trap Type`.
- Analyze the average number of mosquitoes per month to identify trends.

#### **Part 2: Statistical Analysis**
- Perform hypothesis testing to determine if WNV occurrence varies significantly across mosquito species.
- Identify correlations between the number of mosquitoes and other variables.

#### **Part 3: Advanced Statistical Analysis**
- **Linear Regression**:
  - Model how independent variables affect mosquito numbers.
  - Discuss model limitations and iterative improvements.
- **Logistic Regression**:
  - Predict WNV presence using independent variables, including mosquito numbers.
  - Evaluate model performance and limitations.

---

## Methodology
- **Exploratory Data Analysis**:
  - Data cleaning, transformation, and visualization using Python libraries such as Pandas, Matplotlib, and Seaborn.
  - Statistical hypothesis testing and correlation analysis.
- **Predictive Modeling**:
  - Implementation of linear and logistic regression models using Scikit-learn.
  - Model evaluation through metrics such as R², precision, recall, and accuracy.

---

## Requirements
- Jupyter Notebook submissions must include:
  - Commented code for clarity.
  - Markdown cells explaining methodology and findings.

---

## Usage
1. Clone this repository to your local machine.
2. Install the required dependencies listed in `requirements.txt`.
3. Explore the Jupyter Notebooks for EDA and modeling insights.

---

## Future Work
- Incorporate additional environmental data, such as weather conditions, to improve WNV predictions.
- Develop interactive dashboards to visualize mosquito and WNV trends in real time.

---

## License
This project is licensed under the MIT License.

Feel free to contribute to the repository by submitting pull requests or opening issues for suggestions!
