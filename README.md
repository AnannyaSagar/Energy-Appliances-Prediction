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

Summary of the project

Data Visualization: 

Data visualization techniques for instance histogram, line graphs, heatmaps, box plots,pie charts etc helps us in understanding the pattern the data follows. Firstly, we used a pie chart plot to look at the type column. Then we used bar plots and boxplots to visualize the other variables, as most of the variables are categorical in nature. Further we went on to look at the other variable like director ,release date,cast and visualized them using bar chart and word cloud
Feature Engineering (Natural Language Processing):
Natural Language Processing techniques are used so that computers can understand human languages. We performed Natural Language processing techniques like cleaning, removing stopwords, stemming, TF-IDF vectorization. Further we went ahead to perform Principal Component Analysis on the features of the vectorised version of the text based columns.

Feature Selection:

Feature selection helps in reducing the number of input variables to decrease the computational cost of modeling and in some cases it improves the performance of the model.
We selected categorical columns like rating, year and type for K-modes clustering. And we selected text based columns description, listed_in, cast and director for K-means and Hierarchical Clustering. 
 
 
 
Optimal number of Cluster Selection:

After training the dataset on KMode and KMeans models and evaluating on the four evaluation metrics- Elbow method, Silhouette Score, Calinski-Harabasz Index, Dendrogram, the optimal number of clusters came out to be 6 for both the models and for KMeans on the basis of majority from Dendrogram and Elbow Method. 
 
Model Clusters :

Using 6 as the optimal number of clusters under Kmode algorithm the 14 rating variables got clustered properly each cluster comprising mostly one kind of rated content except cluster 1 and 6 comprises Movies and Tv Shows of various ratings. Under KMeans algorithm the Cluster 1 comprises mostly of Documentaries and Musical Documentaries, cluster 2-Dramas and International Movies,cluster 3- Children and Family Movies,cluster 4-Children and Family Movies,cluster 5-International Tv Shows and Tv Dramas, cluster 6-Stand Up Comedy and Talk Shows.

Prediction And Recommendation :-

Recommendation engines basically filter the data and recommend most relevant results to users. These results are recommended in such a manner that likelihood of interest results in maximum. We created a recommendation system by Using Cosine similarity matrix.Cosine similarity is a metric used to measure how similar two items are. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The output value ranges from 0–1. When we provided a movie name ‘Handsome Devil’ then in recommendation we get similar type of genre movie like Secret time, homecoming king, live in new york….etc  in recommendation  
