# Maryland Statewide Vehicle Crashes (2015-2022) 

## Thomas Nguyen | Data 606 | Summer 2023 Capstone in Data Science 

Data Source: https://opendata.maryland.gov/Public-Safety/Maryland-Statewide-Vehicle-Crashes/65du-s3qu

Youtube Video Link: 

Powerpoint link: https://github.com/tnguye53/Thomas_Data606/blob/main/docs/data606_captstone.pptx

Github repo: https://github.com/DATA-606-SUMMER-2023/Thomas_Data606 


![image](https://github.com/tnguye53/Thomas_Data606/assets/54851527/02a15d39-0f38-4577-bdd0-583ebb69c068)

# Abstract
In the state of Maryland, vehicle crashes have risen a significant amount each year. Tens of thousands of collisions reported on average in the state of Maryland. Incidents that occurred in the statewide vehicle dataset examines factors like location, weather conditions, and time contributing the causes of crashes and trends. With modern technology, assessing the severity of crashes and vehicles involved, we can aim to identify potential risk that occurred in different counties of Maryland. The main objective of this project is to provide and predict the types and severity of crashes in the state of Maryland using ML. Predictions will help audiences understand the nature of accidents that occurred through various types of accidents. 

# Introduction
Maryland, located in the Mid-Atlantic region of the United States, is known for its diverse landscapes, scenic mountains, bustling city, and high volume of traffic. The state economy thrives on varies industries like healthcare, technology, biotechnology, and many innovation and research. Given the high volume of individuals across many industries, commuting between counties in Maryland may result in many accidents throughout all times of the day. 

According to Insurify, Gardner and Vohra who are data experts in vehicle, property, and  insurance specialist demonstrated that Maryland ranks sixth-highest in at-fault accident on record. This is 19% higher than national average and the number of people killed in traffic accident is 1 in 10,870. 

# Overview of Data Source
The crash data for Maryland is obtained from https://opendata.maryland.gov/. Crash data in Maryland are reported from January 2015 through December 2022. The dataset contains total of 56 columns and 878343 entries. The dataset is downloaded as a CSV file. In the state of Maryland, on average there are 115,555 car accidents each year over five-year period. This is one of the highest percentage of car crashes on highways and county roads.

## Use of Data

### Columns: 
<table> 
<tr></tr>
<tr><td>

| Features| 
| --- |
| **COUNTY_DESC:** Counties in Maryland (Montgomery, Frederick, Howard, etc.) |
| **YEAR:** Values of year the crash occurred 2015-2022 |
| **QUARTER:** Values of each quarter (Q1, Q2, Q3, Q4) |
| **COLLISION_TYPE_DESC:** Description of collision (Head on righ turn, same direction rear end, etc.) |
| **RD_COND_DESC:** Description of the road condition (No defects or defects) |
| **RD_DIV_DESC:** Description of road divided (Two-way, divided, one-way) |
| **LIGHT_DESC:** Description of light time (Daylight, Dark, etc.) |
| **SURF_COND_DESC:** Description of surface condition (Dry, wet, etc.) |
| **WEATHER_DESC:** Description of weather condition (Blowing sand, clear, raining) |
| **HARM_EVENT_DESC1:** Description of the cause of accident |
| **HARM_EVENT_DESC2:** Description of the cause of accident2 |
| **FEET_MILES_FLAG_DESC:** Description of feet or miles |
| **FIX_OBJ_DESC:** Description of property near accident |
| **ACC_DATE:** Accident Date |
| **ACC_TIME:** Accident Time |
| **SIGNAL_FLAG_DESC:** Yes or No, if direction was flagged |
| **C_M_ZONE_FLAG:** Contains values of N or Y |
| **DISTANCE_DIR_FLAG:** Distance of direction flagged (N, S, E, W) |
| **JUNCTION_DESC:** Description of juntion (Alley, intersection, etc.) |
| **LOG_MILE:** Distance of accident from survey zone |
| **LOGMILE_DIR_FLAG_DESC:** Description of direction accident occurred (North, South, West, East) |
| **DISTANCE:** Distance of the crash |
| **REFERENCE_ROAD_NAME:** References of road name |


</td><td>
  
| Data Types | 
| --- |
| object |
| int64 |
| object |
| object |
| object |
| object |
| object |
| object |
| object |
| object |
| object |
| object |
| object |
| int64 |
| object |
| object |
| object |
| object |
| object |
| object |
| object |
| object |
| object |
  
</td>
</tr>
</table>


<table> 
<tr></tr>
<tr><td>
  
| Target | 
| --- |
| **REPORT_TYPE:** Type of accident reported (Property or Severe crash) |

</td><td> 

| Data Types | 
| --- |
| object |


</td>
</table>

# EDA - Exploratory Data Analysis 
### Steps:
- Extract the data source from openmaryland in form of CSV file and load it into pandas dataframe
- Identify the dataset by using functions like info, describe, shape, isnull to peform analysis
- Check for columns that has null values. If so, columns that have null values will be filled as 'Unknown'
- Produce visualization with dataset
- Develop insights by cleaning and manipulating the dataset to perform ML model 

### Research Question(s):
Given the data source, there are few questions in my analysis that I would like to address:
1.  What is the number of crashes that occurred for each county?
2.  Number of crashes for each year?
3.  Does inclement weather condition impact more crashes?
4.  What is the county with the most crashes?

Link for visualizations: https://github.com/tnguye53/Thomas_Data606/tree/main/docs/visualization

# Techniques and Models
The Machine Learning Models implemented for predicting Maryland Statewide Vehicle Crashes are three classification models. 

## Crash Severity Classification: 
1. Random Forest
2. Logistic Regression
3. Decision Tree

The various classification models selected will be executed to create statistical analysis, visualizations, accuracy, ROC curve, and confusion matrix. Based on the performance of the machine learning models, we chose the best fit model from precision (performance), recall, f1-score, and accuracy. 

# Results of Models 
We performed the three machine learning classification models (Random Forest, Logistic Regression, and Decision Tree) on the features (parameters) to predict our target variable. Classification model are showed along with accuracy score, ROC curve, and area of ROC Curve. 

### Classification Models:

Accuracy of Random Forest algorithm is about **72%**

<img src="/ml/random_forest_result.jpg" width="650" height="350">

Accuracy of Logistic Regression algorithm is about **72%**

<img src="/ml/logistic_regression_result.jpg" width="650" height="350">

Accuracy of Decision Tree model algorithm is about **68%**

<img src="/ml/decision_tree_result.jpg" width="650" height="350">


### ROC Curve:

**ROC Curve for Random Forest**

<img src="/ml/roc_curve_random_forest.jpg" width="400" height="350">

**ROC Curve for Logistic Regression**

<img src="/ml/roc_curve_logistic_regression.jpg" width="400" height="350">

**ROC Curve for Decision Tree**

<img src="/ml/roc_curve_decision_tree.jpg" width="400" height="350">


### Confusion Matrix 

The confusion matrix displays the predicted and actual values of the best performed model. (Property Damage Crash vs Severe Crash)

<img src="/ml/confusion_matrix_blues.jpg" width="400" height="300">

# Conclusion
Based on the overall results, random forest model and ROC curve value of .67 suggest that it provides a better discrimination compared to logistic regression and decision tree. 

Although, logistic regression and random forest classification have the same accuracy of .72 (72%), comparing the ROC curve of .67 (67%) a higher ROC curve indicates a better distinction between positive and negative classes. The model provides a higher probability of correctly classifying 'Severe Crash' as positive instances.

Random Forest classification model is the better model to proceed with as it has higher ROC curve value indicating better overall performance in the target variable.

# Next Steps
In order to pursure further research and obtain better perform: 
- Think of other ML and analysis to perform with the dataset 
- Explore new features that could improve performance
- Obtain more data each year for better accuracy

# References
- https://www.richinandgaines.com/blog/2022/09/maryland-ranks-6th-in-the-nation-for-car-crashes/
- https://insurify.com/insights/states-car-accidents-2022
- https://opendata.maryland.gov/Public-Safety/Maryland-Statewide-Vehicle-Crashes/65du-s3qu
- https://www.trollingerlaw.com/car-accident-statistics/#:~:text=The%20most%20current%20car%20crash,county%20roads%20(23%20percent).
