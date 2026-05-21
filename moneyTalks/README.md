# EPL Survivor Analysis
Regression study of the 9 Premier League clubs that avoided relegation every season from 2013/14–2023/24. \I test whether wages, managerial tenure, or squad experience best explain points variation within this 10 Season window.


## Requirements
`install.packages(c("ggplot2", "car", "e1071", "ggcorrplot"))`
Open notebooks/EPL_Analysis.Rmd and knit to PDF.


## Pipeline
+ Univariate analysis — histograms + skewness check on all 4 variables (Manager Tenure log-transformed due to skewness of 3.16)
+ Bivariate plots — boxplots by team, scatterplots testing wage/tenure/experience vs points
+ Functional form tests — Loess, Linear, Quadratic, and Log fits compared via nested F-tests (ANOVA)
+ OLS with Fixed Effects — club identity included as a dummy variable to isolate marginal resource effects
+ Diagnostics — residual plots, Q-Q plots, Durbin-Watson, VIF checks with mean centering

## Key Findings
> $\color{red}{Club\ identity\ is\ the\ dominant\ predictor}$ - fixed effects are highly significant (p < .001). Crystal Palace starts ~37 pts below Arsenal baseline; Man City starts ~13 pts above.

>$\color{red}{Wages\ become\ insignificant\ once\ club\ identity\ is\ controlled}$ - Log_Wage p = 0.387. High wages reflect club size, not gains from seasonal performance.

>$\color{yellow}{Managerial\ tenure\ has\ no\ significant\ effect}$ - p = 0.229. The "managerial stability" hypothesis is not supported in this season window.

>$\color{yellow}{Squad\ experience\ also\ insignificant}$ - p = 0.856. Experience ratio adds no predictive value after controlling for club identity.

### Data
9 clubs × 11 seasons = 99 observations. Variables: Points, Wage Ratio, Manager Tenure (days, Sept 2 snapshot), Relative Experience Index. 
Source: Soccerdata API + manual wage data.
