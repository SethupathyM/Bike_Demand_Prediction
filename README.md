# Bike_Demand_Prediction

Building a model to predict Bike demand in Seoul city for a day that enables the organization to provide the city with a stable supply of rental bikes and improves customer experiences.

# Problem Statement

Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

# Attribute Information

Date : year-month-day

Rented Bike count - Count of bikes rented at each hour

Hour - Hour of he day

Temperature-Temperature in Celsius

Humidity - %

Windspeed - m/s

Visibility - 10m

Dew point temperature - Celsius

Solar radiation - MJ/m2

Rainfall - mm

Snowfall - cm

Seasons - Winter, Spring, Summer, Autumn

Holiday - Holiday/No holiday

Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

# Used Z-Score technique to remove outliers

Our dataset has many outliers which could affect the effectiveness of the
model. So, by using bar plot outliers had been detected and by using Z- score
technique all the outliers had been imputed with median.

![image](https://user-images.githubusercontent.com/102578847/202542242-ddc70683-0cfd-4cf4-b0bb-62854908f1d6.png)

# Performed One Hot Encoding
![image](https://user-images.githubusercontent.com/102578847/202543133-238d56d4-4975-44fe-9d4b-fe8b3c364064.png)

# Model Implementation and Evaluation

| Model Name  | MSE  | Train R2 score | Test R2 score | Adjusted R2 score
| :------------: |:---------------:| :-----:| :-----:| :-----:|
|Linear Regression | 133073 | 0.66 | 0.65 | 0.64 |
|Polynomial Regression | 70534 | 0.84 | 0.82 | 0.82
|Random Forest Regressor | 20.37 | 0.90 | 0.87 | 0.86|
|Gradient Boost Regressor | 24.19 | 0.86 | 0.84 | 0.84|

# Conclusion

Built a model with Adjusted R2 score of 82% using Polynomial regression. And found top three important features that determine the bike demands are Temperature, Humidity, Functioning day.

