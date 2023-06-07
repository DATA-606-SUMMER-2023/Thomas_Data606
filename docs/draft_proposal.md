# Draft Proposal for Capstone Project

**Name:** Thomas Nguyen 

**Course:** Data 606 

**Instructor:** Dr. Charojie (Jay) Wang


# <img src="https://logodownload.org/wp-content/uploads/2016/11/formula-1-logo-5-2.png" width="250" height="150"> 

# ![image](https://github.com/tnguye53/Thomas_Data606/assets/54851527/183f17b8-6693-4564-8682-514819cc3f71)


# Project - Predicting Qualifying Time and Race Results (1980-2022)

# Overview: 
Formula 1, often abbreviated as F1, is known as the pinnacle of motorsport racing. It is one of world's most prestigious international single-seater auto racing. Formula 1 world championship is organized by Federation International Automobile (FIA), which consist of multiple races called Grand Prix, held on various circuits around the world. The championship is won by teams and each with two drivers. These technical teams design, develop, test, and race their built cars, which are subject to strict regulations and budget cap by FIA. Qualifying sessions in F1 determines the starting positions for each car on the grid for race day. During qualifying, setting the fastest lap time determines the starting position for the grid, so it is crucial as it sets the stage for the race and significantly impact driver's success of being a Grand Prix winner on race day. Therefore, this model will provide whether qualifying time and race winners have a significant impact. 

# Importance of Qualifying and Race Winners: 
Qualifying is extremely important to numerous stakeholders in Formula 1, including championship teams, drivers, fans, key sponsors, and media. The three key factors why qualifying impacts various stakeholders in F1 are teams, drivers, and partnership. 

First, a higher qualifying position increases the chances of scoring more championship points, which contributes to success in team's overall position when it comes to constructors championship. Starting higher on the grid on race day will maximize their chances of winning. Second, a good qualifying time boosts driver confidence and morale because it plays a vital role in team performances. It reduces the risk of incidents and increases their chances of scoring valuale points. Thirdly, sponsors and partnership exposes great drivers when qualifying for the fastest time, which enhances the opportunities for business partners and viewership. 
1. Higher chance of maximizing success in race results 
2. Enhances driver performance and confidence 
3. Attracts attention from sponsors, fans, partners, and gain viewership 

# Data Source: 
- **Source:** Formula 1 datasets is compiled from http://ergast.com/mrd/ obtained through kaggle. The data consist of 14 CSV files that contains a total of 120 columns. However, for the purpose of this project we will be using ***7*** dataset where they contain **circuits, drivers, qualifying, races, results, pit_stops and status**
- **Dataset:** 
  - **Size:** 175.7+ MB 
  - **Columns:** 12 columns 

- **Variables and Dtypes in Dataset**: 
  - result_id (int64): A unique Id of the results for each driver 
  - year (int64): Year for each race 
  - grand_prix (object): The actual name for each circuit 
  - circuit_name (object): Name of circuit 
  - country (object): Country each circuit is located
  - q1 (object): Time in qualifying 1 
  - q2 (object): Time in qualifying 2 
  - q3 (object): Time in qualifying 3 
  - driver_name (object): The drivers first name and last name 
  - starting_position (int64): Starting position of where each driver starts on race day
  - final_position (object): Final position of where each driver finishes on race day
  - status (object): Race status for each driver 
  


#  Techniques and Models: 
- Classification

# Use of the dataset: 
For the Formula 1 dataset, the columns provided to perform our model of Random Forest Classification, there are few labels and features for performing the model to predict the impact of qualifying time and race results. 

**Labels and Variables to perform our Model** 
1. Random Forest Classifier

**Random Forest Classification**: 
For predicting the impact of qualifying time on race results, performing Random Forest classifier the features and target will include a combination of the following: 

Features:
- **grand_prix**: The actual name for each circuit 
- **q1**: Time in Qualifying 1
- **q2**: Time in Qualifying 2
- **q3**: Time in qualifying 3 
- **duration**: How long each driver are in the pits 
- **num_spots**: Number of times each drivers stops during race
- **starting_position**: Starting position of where each driver starts on race day

Target: 
- **final_position**: Final position of where each driver finishes on race day

# Task: 
- Data cleaning and wrangling 
- Understanding data sources 
- Prepare feature and target variables
- Split data into train and test data 
- Perform models 
  - Regression: linear regression 
  - Classification: random forest classifier
- Check for best performance

# Research Question(s):  
- Who has top podium finishes? 
- Who has top qualiyfing lap times on each track? 
- Does driver who secure pole position go on to win the race? 
- Does starting position set during qualifying session impact driver's chances of achieving top position or podium? 

# Outcome: 
The goal of this project is to demonstrate whether setting the fastest qualifying time impacts Grand Prix winners on race day. We will be predicting whether qualifying time (Q3) will result in Grand Prix or race winners. Audiences will be able to summarize the relationship between qualifying times and race winners on analysis performed. 


# References: 
- https://corp.formula1.com/about-f1/
- https://www.fia.com/events/fia-formula-one-world-championship/season-2023/2023-fia-formula-one-world-championship
- https://www.bruinsportsanalytics.com/post/formula1_qualifying
- https://www.f1-fansite.com/f1-teams/f1-teams-2023/
