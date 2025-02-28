# Hotel Booking Data Analysis & Visualization Dashboard

## Overview
This project is a hands-on data analyst portfolio piece where we develop a full end-to-end solution using hotel booking data. We start by creating a SQL Server database from Excel files, then develop SQL queries to prepare our data, and finally connect that database to Power BI. The goal? To answer key stakeholder questions through an interactive visual dashboard.

## Business Questions Addressed
- **Is our hotel revenue growing by the year?**  
  Analyze revenue trends over time.
- **How does revenue break down by hotel type?**  
  Segment revenue for our two hotel types (e.g., City Hotel vs. Resort Hotel).
- **Should we increase our parking lot size?**  
  Investigate trends in guests arriving with personal cars.
- **What general trends can we see?**  
  Explore seasonality via average daily rate (ADR) and guest counts.

## Data Sources & Tools
- **Data Source:**  
  An Excel workbook containing several years (2018–2019, with a sample of 2020) of hotel booking data including room nights (weekday & weekend), ADR, market segments, and meal costs.
- **Tools Used:**  
  Microsoft SQL Server Management Studio is used to create the database, import Excel data, and develop SQL queries.  
  - **SQL:** To merge, clean, and aggregate our data into a unified table.  
  Power BI connects to the database, transforms data, and builds interactive visualizations (dashboards).

## Project Pipeline
1. **Database Creation & Data Import:**  
   - Create a new SQL database (named, for example, "HotelProjects").  
   - Import the Excel sheets using SQL Server’s Import Data Wizard (select Microsoft Excel 2016 as the data source) to load tables like historical bookings, market segments, and meal costs.

2. **Data Preparation Using SQL:**  
   - Run SQL queries to inspect the imported tables.
   - Use `UNION` to append data from multiple years (e.g., 2018, 2019, 2020) into one unified dataset.
   - Calculate key metrics, such as revenue (by multiplying room nights by the ADR, optionally adjusted for discounts).
   - Group data by fields like arrival year and hotel type to answer stakeholder questions.

3. **Connecting to Power BI & Dashboard Creation:**  
   - Use Power BI’s “Get Data” feature to connect to the SQL Server database with the advanced option to input our SQL query.
   - In Power BI, create visuals including:
     - **Line Charts:** To show year-over-year revenue trends.
     - **Segmented Charts:** Breaking revenue down by hotel type.
     - **Additional Visuals:** Displaying metrics like ADR, total room nights, average discounts, and even car parking usage.
     - **Interactive Filters/Slicers:** Allowing stakeholders to filter by date, hotel type, or market segment.

4. **Final Touches:**  
   - Refine the dashboard aesthetics, adjust numeric formats (e.g., rounding, currency formatting), and align visuals to tell a clear, concise data story.
   - Summarize key findings and recommendations in the dashboard for easy stakeholder review.
