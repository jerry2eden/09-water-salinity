# California Cooperative Oceanic Fisheres Investigations

## Aim of the project

To build a predictive model to determine the salinity of sea water and factors affecting changes in salinity

## Data Description


The California Cooperative Oceanic Fisheries Investigations (CalCOFI) data set represents the longest (1949-2016) and most complete (more than 50,000 sampling stations) time series of oceanographic and larval fish data in the world. The physical, chemical, and biological data collected at regular time and space intervals quickly became valuable for documenting climatic cycles in the California Current and a range of biological responses to them. CalCOFI research drew world attention to the biological response to the dramatic Pacific-warming event in 1957-58 and introduced the term “El Niño” into the scientific literature.

The dataset consists of two csv files, bottle.csv and cast.csv. More details about the data can be found [here](https://github.com/HamoyeHQ/09-water-salinity/tree/master/data)

## Our Approach

  * Exploratory Data Analysis
  * Data Visualization
  * Data Preprocessing
  * Modelling
  * Deployment
  
### Exploratory Data Analysis
This was carried out to  better understand the data. Some of the details we checked for were 
  * Shape of the data
  * General information on the data
  * Statistical summary of the data
  
### Data Visualization

Here we visualized the data to find relationships betweeen features and gained more insight into the data. 

**Relationship between Salinity and Temperature**

![Relationship between Salinity and Temperature](https://github.com/Justus-coded/09-water-salinity/blob/master/images/sal%20vs%20temp.jpg)

### Data Preprocessing
Here we checked for inconsistencies in the data and corrected them accordingly. Some of the preprocessing done were:
 * Renaming columns
 * Handling missing values by dropping columns with more that 70% nan and filling nan with mean values
 * Normalization and Standardization

### Modelling
We carried out predictive analysis on the data using various algorithms. We also checked for the feature importance for some algorithms. Based on the cross validation score XGBoost had the best performance. Below is the diagram for feature importance for XGBoost.

**XGBoost Feature Importance**

![XGBoost Feature Importance](https://github.com/Justus-coded/09-water-salinity/blob/master/images/Feature%20importance.JPG)

#### Time Series Analysis
Time series analysis was done using the cast dataset. Predictions were made based on year using Prophet. Below is the diagram showing for cast per week, month and year.

**Time Series Analysis**

![Time series forcast](https://github.com/Justus-coded/09-water-salinity/blob/master/images/TS%202.JPG)

### Pipeline Building
Our pipeline was built using Keras sequential API, a deep learning API running on top of the machine learning platform TensorFlow. The components were built locally on the jupyter notebook as opposed to using a docker image, due to lack of computing power. Our model is ready for deployment using kuberflow and is reusable. However we could not test this model as a result of using gcp free tier




