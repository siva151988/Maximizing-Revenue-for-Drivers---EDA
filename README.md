# Exploratory Data Analysis
## Maximizing Revenue for Drivers
#### DOMAIN : Transportation
#### OBJECTIVE:
The purpose of this Exploratory Data Analysis is to **maximize revenue streams for taxi drivers**. Our goal is to determine whether payment type has impact on fare pricing by focusing on the relationship between payment type and fare pricing.

#### DATA OVERVIEW:
For this analysis, we utilized the Comprehensive dataset of **NYC Taxi Trip records**, used data cleaning and feature engineering procedure to concentrate on essential columns needed for investigation.

#### DATA DICTIONARY:

Displaying only the relevant coulmns

#### passenger_count      : The number of passengers in the Vehicle
#### tpep_pickup_datetime : The date and time when the meter was engaged.
#### tpep_dropoff_time    : The date and time when the meter was disengaged.
#### trip_distance        : The elapsed trip distance in miles reported by taxi meter.
#### payment_type         : The numeric code signifying how the passenger paid for the trip.
#### fare_amount          : The time and distance fare calculated by the meter.

## KEY LEARNINGS:
#### Feature Engineering:
Feature Engineering refers to the process of using domain knowledge to select and **transform the raw data into relevant information that can be used in the analysis**.some variables might not relevant which gets transformed.

Reference from the project : Create new features like trip duration.

#### Data Cleaning:
Data Cleaning is the process of identifying and correcting or removing errors,inconsistencies, and inaccuracies in a dataset. some variables may need **data type conversion, converting the existing data into particular format,** and null values neeeds to be dropped or replaced with mean/median/mode, not all null values need to be replaced with mean/median/mode. 

Reference from the project : Removed rows with missing critical fields such as pickup/dropoff datetime, fare amount, and payment type. Filtered invalid entries from passenger_count, trip_distance and fare_amount.i.e.
     - `passenger_count` <= 0 or > 6
     - `trip_distance` <= 0
     - `fare_amount` <= 0
- Converted object/string columns to datetime format:
  - `tpep_pickup_datetime` to format ['%m/%d/%Y %I:%M:%S %p']
  -  `tpep_dropoff_time` to format ['%m/%d/%Y %I:%M:%S %p']
- Converted numeric codes to renamed label:
  - The payment type has been labeled to Card and Cash
 
#### Outliers:
Outliers are unusual values in your dataset which can distort statistical analyses. We identify and remove them during EDA.

## 🧪 Methodology

| **Step**              | **Description**                                                                                                                                     |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Descriptive Analysis** | Performed statistical analysis to summarize key aspects of the data, focusing on fare amounts and payment types.                                 |
| **Hypothesis Testing**   | Conducted a T-test to evaluate the relationship between payment type and fare amount, testing the hypothesis that different payment methods influence fare amounts. |

## 🚕 Journey Insights
Customers paying with cards tend to have a slightly higher average trip distance and fare amount compared to those paying with cash.

This indicates that customers prefer to pay more with cards when the fare amount and trip distance are higher.

📊 Summary Statistics
| **Metric**	  | **Payment Type**   | **Mean**  |	**Standard Deviation**  |
|---------------|--------------------|-----------|--------------------------|
|Fare Amount	  |   Card	           |   13.70	 |     6.50                 |
|Fare Amount	  |   Cash	           |   12.25   |     6.20                 |
|Trip Distance	|   Card	           |   3.23    |     2.32                 |
|Trip Distance	|   Cash	           |   2.80    |     2.23                 |



## 💳 Preference of Payment Types
The proportion of customers paying with cards is significantly higher than those paying with cash.

Card payments account for 67.5% of all transactions, while cash payments account for 32.5%.

This indicates a strong customer preference for card payments, possibly due to:

Convenience

Enhanced security

Incentives or discounts offered for card usage



## 👥 Passenger Count Analysis
Among card payments, rides with a single passenger (passenger_count = 1) make up the largest proportion — 40.08% of all card transactions.

For cash payments, single-passenger rides account for 20.04% of all cash transactions.

There is a noticeable decrease in the percentage of transactions as the passenger count increases, indicating that larger groups are less likely to use taxis or may prefer alternate payment methods.

These insights highlight the importance of considering both payment type and passenger count when analyzing ride data to understand customer behavior and preferences.



## RECOMMENDATIONS FROM ANALYSIS
**Encourage credit card usage**
Motivate customers to pay with credit cards to leverage higher fare amounts and longer trip distances — helping taxi drivers earn more revenue.

**Offer incentives or discounts**
Implement strategies like promotional discounts or loyalty rewards for credit card transactions to incentivize usage of this payment method.

**Enhance payment experience**
Provide seamless and secure credit card payment options to improve customer satisfaction and encourage greater adoption.
