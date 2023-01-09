# Energy-Appliances-Prediction
Data-driven prediction of energy use of appliances.The data set is at 10 min for about 4.5 months. The house temperature and humidity conditions were monitored with a ZigBee wireless sensor network. Each wireless node transmitted the temperature and humidity conditions around 3.3 min. Then, the wireless data was averaged for
10 minutes periods. The energy data was logged every 10 minutes with m-bus energy meters.Weather from the nearest airport weather station (Chievres Airport, Belgium) was downloaded from a public data set from Reliable Prognosis (rp5.ru) and merged together with the experimental data sets using the date and time column. Two random variables have been included in the data set for testing the regression models and to filter out non-predictive attributes(parameters).

date- time year-month-day hour:minute:second

Appliances- energy use in Wh (Dependent variable)

lights- energy use of light fixtures in the house in Wh (Drop this column)

T1 - Temperature in kitchen area, in Celsius

RH1- Humidity in kitchen area, in %

T2- Temperature in living room area, in Celsius 

RH2-Humidity in living room area, in %

T3-Temperature in laundry room area

RH3- Humidity in laundry room area, in %

T4- Temperature in office room, in Celsius 

RH4-Humidity in office room, in %

T5- Temperature in bathroom, in Celsius

RH5-Humidity in bathroom, in % 

T6- Temperature outside the building (north side), in Celsius

RH6 -Humidity outside the building (north side), in %

T7-Temperature in ironing room , in Celsius

RH7-Humidity in ironing room, in % 

T8- Temperature in teenager room 2, in Celsius 

RH8-Humidity in teenager room 2, in %

T9-Temperature in parents room, in Celsius

RH9-Humidity in parents room, in % 

Tout -Temperature outside (from Chievres weather station), in
Celsius Pressure (from Chievres weather station), in mm Hg 

RHout-Humidity outside (from
Chievres weather station), in %

Wind speed-(from Chievres weather station), in m/s

Visibility-(from Chievres weather station), in km

Tdewpoint-(from Chievres weather station), Â°C

rv1- Random variable 1, nondimensional

rv2- Random variable 2, nondimensional


 Summary of the Project
 
 
Data Visualization: 

Data visualization techniques for instance histogram, line graphs, heatmaps, box plots, etc helps us in understanding the pattern the data follows. Firstly, we used a histogram plot to look at the distribution followed by the target variable - ‘Appliances’. Then we used line plots to visualize the energy consumption of Appliances for each month per day. Further we went on to look at the energy consumption for each day of the week.
Feature Engineering:  
Feature engineering is a method of converting raw data into desirable features before fitting it into a machine learning model which results in better performance. We used feature engineering techniques like binning of numerical data. Additionally we used one hot encoding for the categorical variables.
Feature Selection:-
Feature selection helps in reducing the number of input variables as to decrease the computational cost of modeling and in some cases it improves the performance of the model. We performed four feature selection techniques:- Filter Method, Wrapper Method, Embedded Method and Burota. After performing feature selection three features were dropped - lights, rv1,rv2,weekday, month, visibility.
Model Evaluation metrics :- 
We Evaluated the model on different metrics which helps us to better optimize the performance, fine-tune it, and obtain a better result. And got the results from the best suitable model for our project. Following are the evaluation metrics for our selected model:-

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error(RMSE)

Root Mean Squared Log Error(RMSLE)

R Squared (R2)
 
Model Selection:-

After training the dataset on twelve  models and evaluating on the five evaluation metrics, the ExtraTree Regressor model came out to be the best model with an R2 score of  .75 and RMSE of .31. Extra Trees Regressor, the features and splits are selected at random.. Since splits are 
chosen at random for each feature in the ExtraTrees Regressor, it’s less computationally expensive than other tree based models.

Model Interpretation :-

We used  Shapley Additive Explanation (SHAP Values) For interpretation of our model.The Shapley value is the average marginal contribution of a feature value across all possible coalitions. The goal of SHAP is to explain the prediction of an instance x by computing the contribution of each feature to the prediction. With SHAP package the calculation is quite simple and straightforward. We only need the model (regressor) and the dataset (X_train) .After calculating the SHAP values we  plotted several analyses that will help us to understand the model.


