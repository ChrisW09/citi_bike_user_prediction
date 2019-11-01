# KDD Panthers (Group 10)
This project is part of the Knowledge Discovery in Databases (ITCS - 6162) course from University of North Carolina at Charlotte.

#### -- Project Status: [Active]

## Project Objective
The Objective of this project is to predict the type of User (Customer = 24-hour pass or 3-day pass user; Subscriber = Annual Member) based on trip duration. We will also try to predict whether a customer would be a potential subscriber based on the frequency of trips and trip durations.

### Methods Used  
* Exploratory Data Analysis
* Data Preprocessing 
* Feature Engineering
* Machine Learning
* Predictive Modeling

### Technologies/Libraries
* python
* pandas, jupyter
* scikit-learn
* numpy
* seaborn
* Scipy
* folium maps

### Data and Source Description 
Link to the dataset: https://www.citibikenyc.com/system-data

The dataset which is used for this project is New York Citi Bike share data which gives an extensive information about following attributes:
* Trip Duration (seconds)
* Start Time and Date
* Stop Time and Date
* Start Station Name
* End Station Name
* Station ID
* Station Lat/Long
* Bike ID
* User Type (Customer = 24-hour pass or 3-day pass user; Subscriber = Annual Member)
* Gender (Zero=unknown; 1=male; 2=female)
* Year of Birth

### CRISP-DM Model

#### 1. Installation:
   - Anaconda 4.5.12 Distribution
   - Python 3.7
   
#### 2. Data understanding and Exploratory Data Analysis

Using the Cross-Industry Standard Process of Data Mining (CRISP-DM) the New York citi bike share dataset is collected, cleaned and engineered, such that a good number of business insights are gathered, of which the following five questions are focused upon:

* Which station has highest usage?
* What is the trip duration?
* Which users have high trip duration?
* Which age group has highest usage?
* Which station has highest registered users?
* What time of the day is the service highly utilized?
* Which borough has the highest service usage?

#### 3. Data preparation

Considering correlation of all the variables, we have considered the trip duration,start and end station id and name, start and end station latitude and longitude, gender,year and target variable usertype.

* We have feature engineered the trip distance based on the latitude and longitude values using the [Haversine Distance](https://en.wikipedia.org/wiki/Haversine_formula).

* We have converted the trip duration from seconds to minutes for the purpose of EDA.

* We have considered the 5 boroughs of New York(Manhattan, Queens, Brooklyn, Bronx and Staten Island) and feature engineered a new column based on specific latitude and longitude boundary values of the 5 boroughs.

#### 4. Machine Learning

As per the data we will be using Supervised Classification Algorithm like Random Forest classifier and Naive Bayes Classifier

#### 5. Evaluation
As per the model we will be using accuracy_score as a metric to evalaute the performance of the model.

#### 6. Conclusion 
To build a model which is acuurate to accomodate above mentioned hypothesis.

#### Contributing Project Members

|Name     | 
|---------|
|[Sriganesh Lokesh](https://github.com/sriganeshlokesh)| 
|[Jignesh Manoj Jain](https://github.com/jignesh-jain) |    
|[Maheshwar Mundhe](https://github.com/maheshwar-mundhe) |    
|[Tejashri Arote](https://github.com/[github handle]) |    
|[Neela Ayshwaria Alagappan](https://github.com/NeelaAyshwaria) |
