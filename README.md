# Bike-Sharing-Demand-Prediction
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.
## Data Description
Date :Year-Month-Day

➢ Rented Bike Count -Count of bikes rented at eachhour

➢ Hour -Hour of the day

➢ Temperature -Temperature in Celsius

➢ Humidity -%

➢ Wind Speed -m/s

➢ Visibility -10m

➢ Dew point temperature-Celsius

➢ Solar radiation -MJ/m2

➢ Rainfall -mm

➢ Snowfall -cm

➢ Seasons -Winter, Spring, Summer,Autumn

➢ Holiday -Holiday/No Holiday

➢ Functional Day -NoFunc(Non Functional Hrs),Fun(FunctionalHrs)
# Project Summary
For a city, either a small or large the demand of Rental Bike prediction is a major concern forthe company which is providing the rental service for bike. The demand of Bike could varybased on the various factors like season, weekday, weekend, month, time of the day,environmental conditions and many more.
<br>In this study, For Bike sharing demand prediction we have a dataset consist of 8760 rows and14 columns. Out of 14 features, 4 are of object type, 4 of int and 6 of float type. The datasetconsists no duplicate and null values.For the analysis, we started with data pre-processing then exploratory data analysis,hypothesis testing, data transformation, model training and hyperparameter tuning.
<br>In this project, we train total 7 models including the baseline models, the insight obtained
from the entire steps are following:
## Final observations:
### Categorical feature
<br>(1) there are total 295 days where the demand is zero, which is equal to the total number ofnon-functioning days. It means, on functioning day there is always some demand.
<br>(2) the minimum demand on functioning day is 2 on day Friday season Autumn
<br>(3) The peak hours are 5 to 9 pm and maximum demand at 6pm. However, in morning themaximum demand at 8 am.
<br>(4) The demand is significantly low at early morning about 4 am ,5 am.
<br>(5) The median demand on no holiday is more than the twice than on the holiday and themaximum demand on no holiday is also 1.5 times the holiday.
<br>(6) In Summer, the average demand is maximum and in winter it is minimum and it totallymake sense because in winter due to very cold climatic condition most people don’t prefer bike.
<br>(7) The average demand is very low on Sunday and maximum on Thursday.
<br>(8)In month 6, the average demand is at peak, which might be because in June there issummer season and the temperature range is in 20-30 degree Celsius.
<br>(9)the demand is very low in month 12,1,2 and then start increasing, it might be becausedecember,january,february are the winter months and demand is very low in winters but after
<br>February the temperature starts rising and due to which the demand is increasing.
### Numerical feature
<br>(10)with increase in temperature the demand kept increases up to 30 degree Celsius after thatthere is decrease in demand observed.
<br>(11) Demands are high during low solar radiation and it decreases with increase in solar radiation
<br>(12) The maximum demand occurs when there is no rainfall or snowfall, However demand drops significantly if there is any rainfall or snowfall.
<br>(13) Demands were high at evening , the favourable conditions are when the wind speed andhumidity are in of 1 to 4 m/s and 30 to 70%.
<br>(14)most of snowfall takes place in winter season however some snowfall happened in Autumn season also.

<br>(15) In summer also there was rainfall of high depth was also observed, which have negative
impact on the business.
### Correlation feature
<br>(16) The maximum correlation value is 0.91 between temperature and dew point temperaturefeature.
<br>(17) month feature least impact the demand as it has the least correlation value with the demand.
<br>(18) Rainfall and snowfall impacts negatively to the demand.
<br>(19) Temperature has the maximum correlation value with demand and second highest ishour feature.
### Model training
<br>(20)Linear, Lasso, Ridge regression model are performing almost similar'
<br>(21) out of all models the xgboost has the best training and test score but the differencebetween these scores is high that indicates that model is overfitting. So, we use the RandomForestRegressor as the final model.
### From model explainability
<br>(22) Temperature is the most important feature for the Rented Bike Demand which also has the highest value of the correlation. 
<br>(23) Maximum demand was at the evening, which is the
second most important feature as per SHAP value.
