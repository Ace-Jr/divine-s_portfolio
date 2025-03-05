The data consists of five tables:
dbo.['2018$'] (2018 hotel data)
dbo.['2019$'] (2019 hotel data)
dbo.['2020$'] (2020 hotel data)
dbo.market_segments$ (market segmentation data)
dbo. meal_cost$ (meal cost information)

Steps I used to analyze the data using SQL

Step 1:
Analyzed all years simultaneously by merging the 2018-2020 datasets into a single dataset using **UNION**.

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
