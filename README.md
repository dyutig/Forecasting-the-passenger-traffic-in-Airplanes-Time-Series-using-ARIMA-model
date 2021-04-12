# Forecasting-the-passenger-traffic-in-Airplanes-Time-Series-using-ARIMA-model
This is a basic project on Time series where a ARIMA model has been used to predict the demand(passenger traffic) in Airplanes. 
The data is classified in date/time and the passengers travelling per month.

In this project, firstly the original data has been plotted where a trend component is found to be present. 
After that, the rolling statistics and ADCF Tests have been conducted to confirm that the given time series is not stationary. 

Thus, to make it stationary, 3 transformations have been tested in this project:

1. Log Scale Transformation:
Test Statistic                  -3.162908
p-value                          0.022235
Critical Value (1%)             -3.486535
Critical Value (5%)             -2.886151
Critical Value (10%)            -2.579896

2. Exponential Decay Transformation:
Test Statistic                  -3.601262
p-value                          0.005737
Critical Value (1%)             -3.481682
Critical Value (5%)             -2.884042
Critical Value (10%)            -2.578770

3. Time Shift Transformation
Test Statistic                  -2.717131
p-value                          0.071121
Critical Value (1%)             -3.482501
Critical Value (5%)             -2.884398
Critical Value (10%)            -2.578960

Amongst the above, exponential decay transformation gave the best results in terms of minimum p-value and nearest values of test statistics and critical values. 
However, for simplicity in terms of reverting back to original data during forecasting, Log Scale Transformation has been used.
After than the time series has been decomposed to work on just the residual part.

Finally 3 forecasting models have been built in this project and their performance has been compared with RSS Value. 

1. AR Model:
Order=(2,1,0) 
RSS=1.5023

2. MA Model:
Order=(0,1,2)
RSS: 1.4721

3. ARIMA Model:
Order=(2,1,2)
RSS: 1.0292

Since, the ARIMA model has performed the best in terms of low RSS value, the results have been predicted using ARIMA model.
(We have 144 data points i.e. the existing data of 12 yrs in months and we wanted to forecast for additional 120 data points or 10 yrs.)



