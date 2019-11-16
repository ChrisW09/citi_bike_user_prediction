# KDD Panthers (Group 10)
This project is part of the Knowledge Discovery in Databases (ITCS - 6162) course from University of North Carolina at Charlotte.

#### -- Project Status: [Active]

## Project Objective
The Objective of this project is to predict the **usertype** (Customer = 24-hour pass or 3-day pass user; Subscriber = Annual Member) based on trip duration. We will also try to predict whether a customer would be a potential subscriber based on the frequency of trips and trip durations.

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
* pytorch
* google colab

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

1 Which are the Top 5 Bike Stations by Number of Starts?

2 Which are the Most Popular Trips?

3 Which borough has the highest service usage?

4 How long are the most users travelling?

5 Which gender uses the service adequately?

6 Which age group has highest usage?

7 What is the average trip duration based on User Type?

8 Which user types have high trip duration?


#### 3. Data preparation

Considering correlation of all the variables, we have considered the trip duration,start and end station id and name, start and end station latitude and longitude, gender,year and target variable usertype.

* We have feature engineered the trip distance based on the latitude and longitude values using the [Haversine Distance](https://en.wikipedia.org/wiki/Haversine_formula).

* We have converted the trip duration from seconds to minutes for the purpose of EDA.

* We have considered the 5 boroughs of New York(Manhattan, Queens, Brooklyn, Bronx and Staten Island) and feature engineered a new column based on specific latitude and longitude boundary values of the 5 boroughs.

#### 4. Machine Learning

As the dataset has 1.2 Million records, we will implementing our model in **Google Colab**.

For building and training the model we will be using **Ensemble Learning**. For initial analysis, we will be applying pipeling to the ensemble learning techniques, namely - **Random Forest Classifier, Bagging Classifier, AdaBoost Classifier and Gradient Boosting Classifier.** 

Out of the 4 classifiers, **Random Forest Classifier** had the highest accuracy score of 86.35% followed by **Bagging Classifier** with an accuracy of 84.60%.

As per the highest accuracy standpoint, we have chosen **Random Forest Classifier** as our base model and have applied GridSearchCV to tune the hyperparameters.

Alternatively, we have implemented an **Artificial Neural Network** using **Pytorch** to our dataset. We have trained the neural network for 100 epochs using 4 hidden layers in a Sequential Manner with a learning rate of 0.01 and with a accuracy score of 92%.

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
|[Tejashri Arote](https://github.com/tejashriarote)|    
|[Neela Ayshwaria Alagappan](https://github.com/NeelaAyshwaria) |
