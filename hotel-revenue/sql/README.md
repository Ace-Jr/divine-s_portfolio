# **Hotel Revenue Analysis (2018-2020)**  

## **Dataset Overview**  
This analysis is based on five tables containing hotel booking and financial data:  

- **dbo.['2018$']** – Hotel data for 2018  
- **dbo.['2019$']** – Hotel data for 2019  
- **dbo.['2020$']** – Hotel data for 2020  
- **dbo.market_segments$** – Market segmentation details  
- **dbo.meal_cost$** – Meal cost information  


## **SQL Analysis Steps**  

### **Step 1: Combining Multiple Years of Data**  
I merged the 2018, 2019, and 2020 datasets into a single dataset using **UNION ** to analyze all years simultaneously.  

```sql
WITH hotels AS (
    SELECT * FROM dbo.['2018$']
    UNION
    SELECT * FROM dbo.['2019$']
    UNION
    SELECT * FROM dbo.['2020$']
)
SELECT * FROM hotels;

Step 2:
Created a revenue column using **Average Daily Rate**(ADR) and total numbers of nights stayed (weekdays + weekends).

SELECT 
    (stays_in_week_nights + stays_in_weekend_nights) * adr AS revenue
FROM hotels;

STEP 3:
To understand the revenue trends, I grouped the data by arrival_date_year and hotel, which sums up the total revenue of each hotel type by each year from 2018 - 2020.

SELECT 
    arrival_date_year,
    hotel,
    ROUND(SUM((stays_in_week_nights + stays_in_weekend_nights) * adr), 2) AS revenue
FROM hotels
GROUP BY arrival_date_year, hotel;

STEP 4:
Merged market_segments & meal_cost table to the hotel table using left join to  provide deeper insights

SELECT * 
FROM hotels
LEFT JOIN dbo.market_segments$ AS ms 
    ON hotels.market_segment = ms.market_segment
LEFT JOIN dbo.meal_cost$ AS mc 
    ON mc.meal = hotels.meal;
