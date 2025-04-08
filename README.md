# Black Friday Sales Prediction

![Black Friday Sales Prediction](https://searchengineland.com/figz/wp-content/seloads/2014/12/black-friday1-ss-1920.jpg "Black Friday Sales Prediction")

## Table of Contents
- [Project Introduction](#project-introduction)
- [Dataset Description](#dataset-description)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Preparation](#data-preparation)
- [Modeling Phase](#modeling-phase)
- [Evaluation Metric](#evaluation-metric)
- [Technologies Used](#technologies-used)
- [Conclusion](#conclusion)

---

## Project Introduction

Black Friday is the informal name for the Friday following Thanksgiving Day in the United States, which falls on the fourth Thursday of November. It has been considered the beginning of the U.S. Christmas shopping season since 1952. Over the years, retailers have capitalized on this day by offering heavy discounts and starting sales as early as midnight.

For a retail store or an e-commerce business, a major challenge is setting product prices that maximize profit during such high-volume sales events. This project aims to predict purchase amounts based on historical sales data, which can help businesses in pricing decisions to increase profits.

---

## Dataset Description

The dataset used in this project was obtained from an online data analytics hackathon hosted by **Analytics Vidhya**. It contains various features such as:

- Age  
- Gender  
- Marital Status  
- Product Categories  
- City Demographics  
- Purchase Amount  

It consists of **12 columns** and **537,577 records**. The target variable is the **purchase amount**, which we aim to predict using different regression models.

---

## Exploratory Data Analysis (EDA)

Key insights derived from the data visualization:

- **Gender:** Approximately 75% of the purchases were made by male users, and only 25% by females. Males also tend to spend more on average.  
- **Marital Status:** Single men spend the most during Black Friday. Spending tends to decrease after marriage, possibly due to added responsibilities.  
- **Age Group:** The age group **25–40** is the most active in terms of spending.  
- **Stay in Current City:** Users who have been in the city for just **1 year** tend to spend more, possibly due to their need to buy new items. Long-term residents (>4 years) show reduced purchase activity.  
- **City Category:** While **City B** contributes the most to overall sales revenue, certain products are purchased more frequently in **City C**.

---

## Data Preparation

- **Label Encoding** was used for categorical features such as `Age`, `Gender`, and `City_Category`.  
- **One-hot Encoding (get_dummies)** was applied to the `Stay_In_Current_City_Years` column.  
- **Missing Values** in `Product_Category_2` and `Product_Category_3` were filled appropriately.

---

## Modeling Phase

- The dataset was split into **training and testing sets** using an 80:20 ratio.  
- Multiple regression models were implemented:
  - **Linear Regression**  
  - **Decision Tree Regressor**  
  - **Random Forest Regressor**  
  - **XGBoost Regressor**

---

## Evaluation Metric

The performance of models was evaluated using **Root Mean Square Error (RMSE)**, a standard metric to measure the accuracy of regression models. RMSE calculates the square root of the average squared differences between predicted and actual values.

---

## Technologies Used

- **Python**  
- **Pandas** – for data manipulation and analysis  
- **NumPy** – for numerical operations  
- **Matplotlib** and **Seaborn** – for data visualization  
- **Scikit-learn** – for preprocessing, modeling, and evaluation  
- **XGBoost** – for implementing the XGBoost regression model  
- **Jupyter Notebook** – for interactive development and analysis

---

## Conclusion

Several regression models were tested in this project:

- **Linear Regression**  
- **Decision Tree Regressor**  
- **Random Forest Regressor**  
- **XGBoost Regressor**

Among these, the **XGBoost Regressor** yielded the best results with the lowest RMSE of **2879**, making it the most effective model for predicting purchase amounts in this scenario.
