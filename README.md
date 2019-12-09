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

Using the Cross-Industry Standard Process of Data Mining (CRISP-DM) the New York citi bike share dataset is collected, cleaned and engineered, such that a good number of business insights are gathered, of which the following eight questions are focused upon:

**1. Which are the Top 5 Bike Stations by Number of Starts?**

![top5](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/img/Top5.png)

Here, we have depicted the 5 highly used start stations in the city of New York. **Pershing Square North** seems to be the most used start station as it is quite close to Grand Central Terminal.

**2. Which are the Most Popular Trips?**

![pop](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/img/Most%20Popular.png)

We have depicted the most frequently taken route. From the above plot, we can see that the round trip from **Soissons Landing to Soissons Landing** is quite frequent.

**3. Which borough has the highest service usage?**

![borough](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/img/Borough.png)

From the above, without any suprise, we can determine that the bikeshare service is highly used in **Manhattan, New York**

**4. How long are the most users travelling?**

![long_trips](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/img/Long%20Travelling.png)

We have binned the trip duration into 3 bins - Normal Trips, Extended Trips and Long Trips. From the above we can observe that **Extended Trips** are taken frequently i.e trips of 30 mins to 60 mins.

**5. Which gender uses the service adequately?**

![gender](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/img/Gender.png)

We have one hot endoded the gender to 0,1, and 2 where 0-Unknown, 1-Male, 2-Female. We can see that **Male** gender are highly using this service.

**6. Which age group has highest usage?**

![age](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/img/Age%20Group.png)

We have binned age into 3 bins namely- Young Adults(min-30), Middle-Aged Adults(31-45) and Old Adults(46-max). We observe that **Middle-Aged Adults** highly use the service followed by Young Adults. we can also observe that Old Adults are not falling back from the other two groups.

**7. What is the average trip duration based on User Type?**

![avg](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/img/Avg%20Trip%20Duration.png)

Here, we have plotted avg trip duration over the the type of user. This can be clearly used to differentiate between Customers and Subscribers as **Subscribers** have a high avg trip duration close **33 mins**.

**8. Which user types have high trip duration?**

![high](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/img/Highest%20Trip%20Duration.png)

We can observe that Subscribers take Extended Trips as compared to Customers who tend to use the service for normal trips.


#### 3. Data preparation

Considering correlation of all the variables, we have considered the trip duration,start and end station id and name, start and end station latitude and longitude, gender,year and target variable usertype.

* We have feature engineered the trip distance based on the latitude and longitude values using the [Haversine Distance](https://en.wikipedia.org/wiki/Haversine_formula).

* We have converted the trip duration from seconds to minutes for the purpose of EDA.

* We have considered the 5 boroughs of New York(Manhattan, Queens, Brooklyn, Bronx and Staten Island) and feature engineered a new column based on specific latitude and longitude boundary values of the 5 boroughs.

#### 4. Machine Learning

As the dataset has 1.2 Million records, we will implementing our model in **Google Colab**.

For building and training the model we will be using **Ensemble Learning**. For initial analysis, we have applied **pipeling** to the ensemble learning algorithms, namely - **Random Forest Classifier, Bagging Classifier, AdaBoost Classifier and Gradient Boosting Classifier.** 

Out of the 4 classifiers, **Random Forest Classifier** and **Bagging Classifier** had the highest accuracy score compared to the rest of the algorithms.

Alternatively, we have implemented an **Artificial Neural Network** using **Pytorch** to our dataset. We have trained the neural network for **100 epochs** using **4 hidden layers** in a Sequential Manner with a **learning rate of 0.01.**

After training the neural network, we have saved the model into a file named [Bikeshare.pt](https://github.com/sriganeshlokesh/kdd_project_team_10/blob/master/Bikeshare.pt). Users can load the model onto their Jupyter Notebook and predict new data.

#### 5. Evaluation

Since we have implemented a classification model, we have evaluated our model using **accuracy_score** from sklearn as a primary metric. Once the model was fit, we have evaluated our model's features to the unseen test labels. 

Considering the ensemble learning algorithm group, we wanted to discover which algorithm performs well in basic conditions without any parameter tuning and found out that **Random Forest Classifier** had the highest accuracy score of 86.35% followed by **Bagging Classifier** with an accuracy of 84.60%.

We also wanted to check how a **deep learning** model performs againest this dataset. Therefore, we implemented an **Artificial Neural Network** using **Pytorch**. The model gave an accuracy of 92%. 

#### 6. Conclusion 

This project has been built by implementing a **pipeline** of ensemble learning algorithms namely - **Random Forest, Bagging, Boosting and an Artificial Neural network**. As per our hypotheses, we built our machine learning and deep learning models inorder to get some insights which can be utilized in profitable business models. 

#### Contributing Project Members

|Name     | 
|---------|
|[Sriganesh Lokesh](https://github.com/sriganeshlokesh)| 
|[Jignesh Manoj Jain](https://github.com/jignesh-jain) |    
|[Maheshwar Mundhe](https://github.com/maheshwar-mundhe) |    
|[Tejashri Arote](https://github.com/tejashriarote)|    
|[Neela Ayshwaria Alagappan](https://github.com/NeelaAyshwaria) |
