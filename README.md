# Customer Shopping Behavior Analysis

## Project Overview
- This project analyzes customer shopping behavior using transactional data from 3,900 purchases across various product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.

---

## Data Summary
- **Rows**: 3,900
- **Columns**: 18
  
 ### **Features**:
 - **Customer Demographics**:
   
   Age, Gender, Location, Subscription Status
 - **Purchase details**:
   
   Item Purchased, Category, Purchase Amount, Season, Size, Color
 - **Shopping Behavior**:

   Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type
 - **Missing Data**:

   37 values in the Review Rating column

---

## **Exploratory Data Analysis using Python**
We began with data preparation and cleaning with python:

 - **Data Loadind**: Imported dataset using `pandas`.
   
 - **Initail Exploration**: Used `df.info()` to check structure `df.describe()` for summary statistics.
   
 - **Missing Data Handling**: Checked for null values and imputed values in the `Review Rating` using the median rating of each product category.
   
 - **Column Standardization**: Renamed columns to snake case for better readability and documentation
   
 - **Feature Engineering**:
   
   - Created `age_group` column by binning customer ages.
     
   - Created `purchase_frequency_days` column from purchase data.
     
 - **Data Consistency Check**: Verified if `discount_applied` and `promo_code_used` were redundant; dropped `promo_code_used`.
   
 - **Database Integration**: Connected Python script to PostgreSQL and loaded the cleaned DataFrame into the database for SQL analysis.   

