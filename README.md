# Chicago Crime Data Time Series Analysis

## Project Overview
This project analyzes Chicago crime data across multiple years (2001-2022) to identify patterns, trends, and insights about criminal activity in the city. The analysis uses time series techniques and exploratory data analysis to answer key questions about crime distribution across districts, time periods, and holidays.

## Dataset
The analysis uses Chicago crime data spanning from 2001 to 2022, with each year stored in a separate CSV file. The dataset includes information about:
- Crime type (Primary Type)
- Location (District, coordinates)
- Date and time of occurrence
- Other relevant crime attributes

## Key Findings

### 1. Police District Analysis (2022)
**Most Crime:** District 8 recorded the highest number of crimes in 2022 with 15,116 incidents, indicating it as a high-priority area for law enforcement resources.

**Least Crime:** District 31 had the lowest crime count with only 54 incidents, suggesting either effective policing, different community characteristics, or lower population density.

<img width="1371" height="571" alt="image" src="https://github.com/user-attachments/assets/4906f1b5-11d5-492f-a563-459150f221ce" />



*Figure 1: Crime distribution across Chicago police districts in 2022*

### 2. Crime Trends Across Years
**Overall Trend:** Crime in Chicago has generally been **decreasing** from 2001 to 2022, with some fluctuations. Notable drops occurred around 2017-2018, with a slight uptick in recent years.

<img width="1371" height="571" alt="image" src="https://github.com/user-attachments/assets/92e012bb-5368-47c5-9eb1-4f99ea05aa32" />


*Figure 2: Total crimes in Chicago from 2001 to 2022 showing overall declining trend*

**Counter-Trend Crimes:** While overall crime decreased, certain crime types showed opposite trends in specific years. For example, some years saw increases in particular crime categories even when total crime was declining, suggesting shifts in criminal activity patterns rather than uniform reduction.

### 3. Rush Hour Crime Patterns
**PM Rush Hour has More Crime:** Analysis of crimes occurring during rush hours reveals that PM rush hour (4-7 PM) experiences significantly more criminal activity than AM rush hour (7-10 AM).

<img width="1570" height="571" alt="image" src="https://github.com/user-attachments/assets/1040a280-8da1-4358-b5a9-626dea0d714b" />

*Figure 3: Comparison of crime counts during AM (7-10 AM) vs PM (4-7 PM) rush hours*

**Top 5 AM Rush Hour Crimes:**
1. Theft
2. Battery
3. Criminal Damage
4. Assault
5. Motor Vehicle Theft

**Top 5 PM Rush Hour Crimes:**
1. Theft
2. Battery
3. Criminal Damage
4. Assault
5. Robbery

**Motor Vehicle Theft:** More common during AM rush hour, suggesting criminals target vehicles when owners are at work or away from their cars for extended periods.

### 4. Monthly Crime Patterns
**Highest Crime Months:** Summer months (July, August) consistently show the highest crime rates, likely due to increased outdoor activity, warmer weather, and more opportunities for crime.

**Lowest Crime Months:** Winter months (January, February) typically have the lowest crime rates, possibly due to colder weather keeping both criminals and potential victims indoors.

<img width="1171" height="571" alt="image" src="https://github.com/user-attachments/assets/6b01a8a8-74b9-4665-b380-679989bef559" />



*Figure 4: Total crimes per month showing seasonal patterns*


<img width="1371" height="571" alt="image" src="https://github.com/user-attachments/assets/564e9951-42ea-4fd4-b300-4cf95f474e22" />

*Figure 5: Monthly trends for the top 5 most common crime types*

**Exceptions to the Pattern:** Certain crime types deviate from the general monthly trend. For instance, some property crimes may peak during different months due to seasonal factors like holiday shopping or vacation periods when homes are left unattended.

### 5. Holiday Crime Analysis
**Top 3 Holidays with Most Crime:**
1. **New Year's Day** - High levels of celebratory gatherings and alcohol consumption contribute to increased criminal activity
2. **Independence Day (July 4th)** - Large public celebrations and fireworks create opportunities for various crimes
3. **Christmas Day** - Despite being a family-oriented holiday, property crimes and domestic incidents occur

<img width="1371" height="571" alt="image" src="https://github.com/user-attachments/assets/71c72212-8d01-46ba-8c2b-7d6ea8744650" />

*Figure 6: Crime counts for major US holidays*

**Most Common Crimes on These Holidays:**
Each of the top 3 holidays showed similar patterns with the top 5 crimes being:
- Theft
- Battery
- Criminal Damage
- Assault
- Narcotics violations

### 6. Time Series Decomposition
**Seasonal Patterns:** The decomposition analysis reveals strong seasonal patterns in Chicago crime data, with clear yearly cycles that repeat consistently.

**Trend Component:** The long-term trend shows a general decline in crime over the analysis period, with some stabilization in recent years.

**Cycle Magnitude:** The difference between peak and trough in the seasonal component indicates significant variation in crime rates throughout the year, with predictable patterns that could inform resource allocation.

<img width="1371" height="990" alt="image" src="https://github.com/user-attachments/assets/320a0323-1a45-4386-9a97-581b67941fa9" />

*Figure 7: Seasonal decomposition of daily crime data showing trend, seasonal, and residual components*

<img width="1371" height="990" alt="image" src="https://github.com/user-attachments/assets/d3e020db-4151-4671-995c-de41c66cce6f" />

*Figure 8: Time series decomposition specifically for theft crimes*

## Methodology
The analysis employed several techniques:
- **Exploratory Data Analysis (EDA):** Counting, grouping, and comparing crime frequencies across different dimensions
- **Time Series Analysis:** Examining trends over time, identifying patterns in daily, monthly, and yearly data
- **Seasonal Decomposition:** Breaking down the time series into trend, seasonal, and residual components to understand underlying patterns
- **Comparative Analysis:** Comparing crime rates across different time periods, locations, and circumstances

## Implications
These findings have several practical applications:
- **Resource Allocation:** Police districts can be prioritized based on crime volume
- **Temporal Deployment:** Law enforcement resources can be strategically deployed during high-crime months and time periods
- **Holiday Planning:** Special security measures can be implemented for high-crime holidays
- **Crime Prevention:** Understanding seasonal and temporal patterns enables proactive prevention strategies
- **Policy Making:** Long-term trends inform policy decisions and evaluation of crime reduction initiatives

## Technical Requirements
The analysis was conducted using Python with the following libraries:
- pandas (data manipulation)
- numpy (numerical operations)
- matplotlib (visualization)
- seaborn (statistical visualization)
- statsmodels (time series analysis)
- holidays (holiday identification)


 ##  Contact
- **Bashar Bayatna**, Mechatronics Engineer | Junior Data Scientist  
- Email: [Basharbayatna11@gmail.com](mailto:Basharbayatna11@gmail.com)


