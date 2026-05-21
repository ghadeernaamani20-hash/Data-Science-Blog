# Data-Science-Blog


# Hospital Patient Satisfaction Analysis

##  Project Motivation
Patient satisfaction is an essential measure of healthcare quality. Hospitals collect large amounts of survey data, but identifying the key factors that drive positive patient experiences can be challenging.

This project analyzes HCAHPS (Hospital Consumer Assessment of Healthcare Providers and Systems) survey data to:
- Understand how satisfaction is distributed across hospitals
- Identify the factors that most influence patient satisfaction
- Build a predictive model to estimate satisfaction levels

---

##  Business Questions
This project aims to answer the following key questions:

1. What is the distribution of patient satisfaction across healthcare facilities?  
2. Does the number of completed surveys influence satisfaction scores?  
3. How does the survey response rate impact patient satisfaction?  
4. Which hospital characteristics are most strongly associated with satisfaction levels?  

---

##  Dataset Description
The dataset contains hospital-level survey data collected through the HCAHPS program. It includes:

- Patient satisfaction scores (percentages)
- Survey participation metrics (response rate, number of surveys)
- Hospital ratings and communication measures

The data is originally in **long format**, where each hospital appears multiple times (once per survey measure), and was transformed into **wide format** for analysis.

---

## Libraries Used
The following Python libraries were used:

- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  

---

##  Data Preparation
The dataset required several preprocessing steps:

- Selection of relevant columns  
- Conversion of numeric fields  
- Removal of missing values  
- Transformation from long format to wide format (pivoting)  
- Aggregation of survey-related features  

---

##  Exploratory Data Analysis
The analysis included:

- Distribution plots of satisfaction scores  
- Scatter plots to examine relationships between variables  
- Correlation analysis to identify key factors  

---

##  Key Findings
- Patient satisfaction scores are approximately normally distributed (mostly between 65%–85%)
- The number of completed surveys has little direct impact on satisfaction
- Higher survey response rates are associated with higher satisfaction
- Communication factors (especially nurse communication) strongly influence satisfaction
- Hospitals with better overall ratings tend to show consistently higher satisfaction across measures

---

##  Modeling Approach
A **Linear Regression model** was used to predict patient satisfaction.

- Features included survey metrics and hospital rating variables  
- The target variable was:  
  `H_COMP_1_A_P` (patients reporting nurses always communicated well)

---

##  Model Performance
- **R² Score:** ~0.74  
- **Mean Squared Error:** ~7.88  

 Interpretation:
- The model explains about **74% of the variation** in patient satisfaction  
- Prediction errors are relatively low, indicating good performance  

 Note:
Some variables are highly correlated because they represent different response categories of the same question. This may introduce **multicollinearity** and slightly inflate model accuracy.

---

##  Example Prediction
A sample hospital scenario was created using realistic values (e.g., survey response rate and rating distribution).

The model predicts:
- The expected percentage of patients who report positive nurse communication

This demonstrates how survey and rating metrics can be used to estimate hospital performance.

---

##  Repository Structure

- `Data/`  
  Contains the dataset used for analysis. Depending on file size, this may include either the full dataset or a sample version.

- `Graphs/`  
  Stores all visualizations generated during the exploratory data analysis (EDA), including distribution plots, scatter plots, and correlation charts.

- `notebook.ipynb`  
  The main Jupyter Notebook containing:
  - Data cleaning and preparation  
  - Exploratory data analysis  
  - Machine learning model development  
  - Model evaluation and prediction  

- `Blog.md`  
  A non-technical explanation of the project, designed for a general audience. It highlights the key findings and insights without going into technical details.

- `README.md`  
  Provides an overview of the project, including objectives, methods, results, and instructions for understanding the repository.
