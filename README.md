# Pesticide
Forecasting Future Pesticide Usage Trend In US

![image](https://github.com/user-attachments/assets/cb8ad58a-bb46-4b7a-a5ab-f3226520c8ad)


This project aims to predict the patterns of pesticide use over time for various chemicals in local catchments and watersheds, to assess levels of contamination. It entails forecasting the spatial and temporal distribution of pesticide concentrations, drawing on historical data on usage and environmental conditions.Companies could utilize predictive analytics on this data to project future trends in pesticide usage. This approach would aid in strategic decision-making concerning production scheduling, inventory control, and market strategy.

# Data Description: 
Data link: https://www.kaggle.com/datasets/konradb/pesticide-usage-in-the-united-states

The data on agricultural pesticide use was gathered through the USGS. This data aims to enhance the understanding of pesticide presence in freshwater and its effects on water availability across the United States.
# This data consists of six variables namely:
1. COMPOUND: This represents the name or type of pesticide compound being used or applied.
2. YEAR: This represents the year in which the pesticide application occurred.
3. STATE_FIPS_CODE: This represents the Federal Information Processing Standards (FIPS) code for the state where the pesticide application took place.
4. COUNTY_FIPS_CODE: This represents the Federal Information Processing Standards (FIPS) code for the county where the pesticide application took place.
5. EPEST_LOW_KG: This represents the lower estimate of the amount of pesticide applied, measured in kilograms.
6. EPEST_HIGH_KG: This represents the higher estimate of the amount of pesticide applied, also measured in kilograms.

# Data Preparation
1. Data Cleaning: The dataset consists of 1,048,576 entries. Missing values were handled using the na.interp function.
2. Time Series Conversion: Data was converted into a time series format with annual data points.
3. Transformation: A logarithmic transformation was applied for normalization.
4. Stationarity: Unit root testing ensured stationarity of the time series.
5. Data Splitting: The dataset was split into an 80% training set and a 20% testing set.
   
# Modeling Approach
The following models were employed in the analysis:

1. Simple Exponential Smoothing (SES)
2. Holt's Linear Trend Model
3. Exponential Smoothing State Space Model (ETS)
4. ARIMA
5. Dynamic Regression
   
After evaluating these models, the ARIMA (1,0,1) model was determined to be the most effective based on the Root Mean Square Error (RMSE) of the back-transformed training data. This model was then used to forecast pesticide usage for the next four years.

# Result
These visualizations depict the historical pesticide usage data, the forecasts produced by the ARIMA model, and the associated confidence intervals. The forecasts provide a clear picture of the expected trends over the coming years.

![image](https://github.com/user-attachments/assets/83c97022-1d4f-4462-9cc9-7f34ccf3cd21)![image](https://github.com/user-attachments/assets/8f85cbbe-63d3-4cee-b5d7-c8be7914afd2)
![image](https://github.com/user-attachments/assets/e1a3d554-b1d8-461d-917e-1a84f6116b14)
![image](https://github.com/user-attachments/assets/40dfdb6f-2fdd-4086-b1fb-95410afa0fef)

# Strategic Implications
The insights derived from this analysis can be highly beneficial for:

Agricultural Companies: To optimize production scheduling, inventory control, and market strategy.
Environmental Agencies: To monitor and manage pesticide levels in water bodies more effectively.

# Future Work
Further Model Evaluation: Compare the forecast accuracy of the ARIMA model with other models using additional performance metrics like MAE and MAPE.
Incorporating External Variables: Integrating factors such as weather patterns, crop types, and economic indicators into the model could enhance forecast accuracy.
Scenario Analysis: Explore different scenarios by adjusting key parameters, such as changes in pesticide regulations, to predict possible future trends.




