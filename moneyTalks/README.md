# Money Talks: Predicting League Performance from Wage Spending

Can money buy success? 
This project explores the famous *Soccernomics* claim that a club’s wage bill is the best predictor of their league position.

## Scope
The focus is on all teams that have not been relegated since the 2013-2014 Season.
Collecting the following data points: Club, Season, Total Wage Bill, League Position, Manager Tenure(In Days), Matches Played and Points.
Optional points(For deeper analysis): Squad Age, GD, XG, Transfer Spent Per Position, Wage Spent Per Position.

### Teams
- Arsenal
- Everton
- Liverpool
- Manchester United
- Tottenham
- Chelsea
- Manchester City
- Crystal Palace
- West Ham

## Methodology
### 1. Manager Tenure(Stability):
To strictly measure "Ex Ante" stability (stability prior to performance), manager tenure is calculated using a **September 2nd Snapshot Rule**:

-**Definition:** Tenure is defined as the consecutive days a manager has held the position as of September 2nd of the target season.

-**Rationale:** This date aligns with the closure of the English Premier League Transfer Window. It effectively attributes the squad's construction and pre-season preparation to the manager in charge at that deadline.

-**Noise Reduction:** This method isolates "Preparation Stability" from "Survival Tenure," preventing reverse causality where match results influence the tenure variable (e.g., mid-season sackings).

### 2.The Relative Experience Index (REI)
Rather than using average age, which fails to capture game intelligence, I engineered a **Relative Experience Index**.

-**Metric:** Cumulative career appearances in Europe's "Top 5 Leagues" (EPL, La Liga, Bundesliga, Serie A, Ligue 1) for all players with >5 apps in the season.

-**Normalization:** Raw experience counts were normalized against the 9-team cohort average for each specific season.
    * *Formula:* `Team_Avg_Experience / Cohort_Avg_Experience

- **Why Normalize?** This controls for the secular trend of increasing career lengths over the seasons, ensuring that a "highly experienced" team in 2014 is comparable to one in 2024.

### 3. Data Integrity & Constraints

-**Leap Year Adjustment:** The algorithms account for the extra calendar day in 2016, 2020, and 2024 to ensure precise tenure calculations.

-**The "Unified Season" Approach:** January transfers are included to reflect managerial adaptability/correction, with their experience metrics retroactively baselined to the season start to maintain temporal consistency.

## Project Roadmap
- Scope Definition & Team Selection
- Data Collection (Web Scraping via Selenium/Soccerdata API)
- Feature Engineering (Tenure Calculations & Leap Year Adjustments)
- Exploratory Data Analysis (EDA)
- Regression Modeling (OLS/Panel Data)
- Final Hypothesis Testing
