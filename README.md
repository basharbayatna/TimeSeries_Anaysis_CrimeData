

<img width="1508" height="1005" alt="image" src="https://github.com/user-attachments/assets/6c76e697-15fd-470c-8d55-e77360060bb8" />






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





##  Forecasting Results: 6-Month Predictions

### Theft Crime Forecast

<img width="1032" height="415" alt="image" src="https://github.com/user-attachments/assets/ee317c58-3cf6-4be3-ac18-38654a566fb6" />

*Figure 9: Monthly Theft Crimes Counts Across the Years*

**Model Used:** SARIMA (Seasonal AutoRegressive Integrated Moving Average)
- **Model Specification:** SARIMA(1,1,0)(1,0,0)[12]
- **Methodology:** Manual parameter selection based on ACF/PACF analysis
- **Training Approach:** 75% training data, 25% test data split

**Forecast Results:**
- **Expected Trend:** Projected **decrease** in theft crimes over the next 6 months
- **Percentage Change:** Approximately **3-5% decline** from current levels
- **Confidence:** 95% confidence interval indicates stable to declining pattern
- **Model Performance:** Low error metrics demonstrate strong predictive accuracy

**Diagnostic Assessment:**
- ✅ Residuals approximately normally distributed
- ✅ No significant autocorrelation remaining
- ✅ Stable variance over forecast period

**Visualization:**
<img width="877" height="415" alt="image" src="https://github.com/user-attachments/assets/a5d14147-10d8-496a-9257-c23d10bbf797" />


*Figure 10: 6-Month Theft Crime Forecast with Confidence Intervals*

---

### Battery Crime Forecast

<img width="1032" height="338" alt="image" src="https://github.com/user-attachments/assets/74f12fbb-30fa-4e9e-be09-dae133fbe5d7" />

*Figure 11: Monthly Battery Crimes Counts Across the Years*

**Model Used:** SARIMA with Auto-ARIMA optimization
- **Model Specification:** SARIMA(1,1,1)(1,0,1)[12]
- **Methodology:** Auto-ARIMA selected optimal parameters based on AIC criterion
- **Training Approach:** 75% training data, 25% test data split

**Forecast Results:**
- **Expected Trend:** Relatively **stable** battery incidents with minimal change
- **Percentage Change:** ±2% variation anticipated
- **Seasonal Influence:** Model captures strong seasonal component suggesting slight summer uptick
- **Model Performance:** Auto-ARIMA achieved lower error metrics than manual specification

**Diagnostic Assessment:**
- ✅ All diagnostic tests passed
- ✅ Model residuals show no patterns
- ✅ Reliable for short-term forecasting

**Visualization:**
<img width="882" height="415" alt="image" src="https://github.com/user-attachments/assets/84160a4c-fab2-470d-b16a-eaa05317f019" />

*Figure 12: 6-Month Battery Crime Forecast with Confidence Intervals*


---

### 4.  Strategic Recommendations**

**ENTIRE SECTION ADDED:**
##  Strategic Recommendations

### For Law Enforcement Agencies

1. **District Resource Allocation**
   - Prioritize staffing and patrol units in District 8 and other high-crime areas
   - Study successful strategies from District 31 and low-crime districts
   - Implement district-specific intervention programs

2. **Temporal Deployment Strategy**
   - Increase patrol presence during PM rush hours (4-7 PM) for general crime prevention
   - Focus motor vehicle theft prevention during AM rush hours (7-10 AM)
   - Prepare for summer crime spikes with seasonal staffing adjustments

3. **Holiday Preparedness**
   - Deploy enhanced resources on New Year's Day, July 4th, and Memorial Day
   - Implement holiday-specific crime prevention campaigns
   - Coordinate with community organizations for holiday safety initiatives

4. **Forecast-Driven Planning**
   - Use theft decline projections to reallocate resources to emerging crime categories
   - Monitor battery crime stability and maintain consistent response capacity
   - Update forecasts quarterly for adaptive resource management

### For Policy Makers & City Officials

1. **Prevention Program Investment**
   - Expand summer youth programs to reduce seasonal crime increases
   - Target community engagement in high-crime districts identified in the analysis
   - Develop evidence-based intervention programs for specific crime types

2. **Data-Driven Budget Allocation**
   - Use crime forecasts to inform annual public safety budgets
   - Allocate resources based on spatial and temporal crime patterns
   - Invest in data analytics infrastructure for ongoing monitoring

3. **Community Partnerships**
   - Collaborate with neighborhood organizations in high-crime districts
   - Launch awareness campaigns during peak crime periods
   - Establish feedback mechanisms for community-driven solutions

4. **Technology & Innovation**
   - Implement predictive policing tools in strategic locations
   - Develop real-time crime monitoring dashboards
   - Invest in evidence-based crime prevention technologies


---

### 5.  Technical Methodology**

**ENTIRE SECTION ADDED:**
## 🛠️ Technical Methodology

### Tools & Technologies
- **Data Analysis:** pandas, numpy
- **Visualization:** matplotlib, seaborn
- **Time Series Analysis:** statsmodels
- **Forecasting:** SARIMA modeling, pmdarima (Auto-ARIMA)
- **Statistical Testing:** Augmented Dickey-Fuller test, ACF/PACF analysis
- **Additional Libraries:** holidays (for holiday detection)

### Analysis Pipeline

1. **Data Integration & Preprocessing**
   - Loaded and concatenated 22 years of crime data (2001-2022)
   - Standardized date formats and extracted temporal features (hour, month, year)
   - Handled missing values and ensured data quality

2. **Exploratory Data Analysis**
   - District-level crime aggregation and comparison
   - Temporal pattern identification across multiple time scales
   - Rush hour and holiday impact assessment

3. **Time Series Decomposition**
   - Applied seasonal decomposition using additive model
   - Extracted trend, seasonal, and residual components
   - Quantified seasonal magnitude relative to overall variation

4. **Stationarity Testing & Differencing**
   - Conducted Augmented Dickey-Fuller tests
   - Determined optimal differencing parameters (d, D)
   - Achieved stationarity for reliable modeling

5. **SARIMA Model Development**
   - Analyzed ACF/PACF plots for parameter selection
   - Built manual SARIMA models based on statistical inference
   - Applied Auto-ARIMA for automated optimal parameter selection
   - Implemented 75-25 train-test split for validation

6. **Forecasting & Validation**
   - Generated 6-month forecasts for Theft and Battery crimes
   - Performed comprehensive model diagnostics
   - Calculated performance metrics (MAE, RMSE, MAPE, R²)
   - Validated forecast reliability with confidence intervals

---

### 6.  Future Enhancements**


## 🚀 Future Enhancements

- Incorporate weather data to analyze environmental impacts on crime
- Implement machine learning models (LSTM, Prophet) for comparison with SARIMA
- Add spatial analysis with geographic clustering and hotspot mapping
- Develop interactive dashboard for real-time crime monitoring
- Include socioeconomic indicators in predictive models
- Extend forecast horizon to 12-24 months for long-term planning
- Analyze crime displacement effects from policy interventions
- Integrate real-time data feeds for continuous model updating


---

### 7.  Key Performance Indicators**


##  Key Performance Indicators

The forecasting models demonstrated strong predictive performance:

**Theft SARIMA Model:**
- Successfully captured seasonal patterns and long-term trends
- Low residual autocorrelation indicating good model fit
- Reliable confidence intervals for decision-making

**Battery SARIMA Model:**
- Auto-ARIMA optimization improved model accuracy
- Strong diagnostic performance across all tests
- Stable predictions suitable for resource planning
  

---

### 8.  Project Outcomes**


## Project Outcomes

This analysis provides actionable intelligence for:
- **Operational Planning:** Data-driven patrol scheduling and resource deployment
- **Strategic Planning:** Long-term crime prevention strategy development
- **Budget Allocation:** Evidence-based funding decisions for public safety
- **Community Engagement:** Targeted outreach in high-priority areas and time periods
- **Policy Evaluation:** Framework for assessing intervention effectiveness



 ##  Contact
- **Bashar Bayatna**, Mechatronics Engineer | Junior Data Scientist  
- Email: [Basharbayatna11@gmail.com](mailto:Basharbayatna11@gmail.com)


