# Final Proposal for Capstone Project

**Name:** Thomas Nguyen 

**Course:** Data 606 

**Instructor:** Dr. Charojie (Jay) Wang

# Maryland Statewide Vehicle Crashes (2015-2022)

# Overview: 
The crash data for Maryland is obtained from https://opendata.maryland.gov/. Crash data in Maryland are reported from January 2015 through December 2022. The dataset contains total of 56 columns and 878343 entries. The dataset is downloaded as a CSV file. 

# Columns: 
**Data source:** https://opendata.maryland.gov/Public-Safety/Maryland-Statewide-Vehicle-Crashes/65du-s3qu

- **YEAR:** Values of year the crash occurred 2015-2022
- **QUARTER:** Values of each quarter (Q1, Q2, Q3, Q4) 
- **LIGHT_DESC:** Description of light time (Daylight, Dark, etc.) 
- **LIGHT_CODE:** Values presented of LIGHT_DESC
- **COUNTY_DESC:** Counties in Maryland (Montgomery, Frederick, Howard, etc.) 
- **COUNTY_NO:** Values presented of COUNTY_DESC
- **MUNI_DESC:** Column contains only null values 
- **MUNI_CODE:** Values presented by MUNI_DESC
- **JUNCTION_DESC:** Description of juntion (Alley, intersection, etc.) 
- **JUNCTION_CODE:** Values presented by JUNCTION_DESC
- **COLLISION_TYPE_DESC:** Description of collision (Head on righ turn, same direction rear end, etc.) 
- **COLLISION_TYPE_CODE:** Values presented by COLLISION_TYPE_DESC
- **SURF_COND_DESC:** Description of surface condition (Dry, wet, etc.) 
- **SURF_COND_CODE:** Values presented by SURF_COND_DESC
- **LANE_CODE:** Values of LANE_CODE
- **RD_COND_DESC:** Description of the road condition (No defects or defects)
- **RD_COND_CODE:** Values presented by RD_COND_DESC
- **RD_DIV_DESC:** Description of road divided (Two-way, divided, one-way)
- **RD_DIV_CODE:** Values presented by RD_DIV_DESC
- **FIX_OBJ_DESC:** Description of property near accident 
- **FIX_OBJ_CODE:** Values presented by FIX_OBJ_DESC
- **REPORT_NO:** Report number presented on file for each accident
- **REPORT_TYPE:** Type of accident reported (Property, fatal, or injury crash) 
- **WEATHER_DESC:** Description of weather condition (Blowing sand, clear, raining) 
- **WEATHER_CODE:** Values presented by WEATHER_DESC
- **ACC_DATE:** Accident Date
- **ACC_TIME:** Accident Time
- **LOC_CODE:** Location code for each county
- **SIGNAL_FLAG_DESC:** Yes or No, if direction was flagged
- **SIGNAL_FLAG:** Short values of yes or No, if signal was flagged (Y or N) 
- **C_M_ZONE_FLAG:** Contains values of N or Y 
- **AGENCY_CODE:** Code represent each county
- **AREA_CODE:** Area Code of each county
- **HARM_EVENT_DESC1:** Description of the cause of accident 
- **HARM_EVENT_CODE1:** Values presented by HARM_EVENT_DESC1
- **HARM_EVENT_DESC2:** Description of the cause of accident 2
- **HARM_EVENT_CODE2:** Values presented by HARM_EVENT_DESC2
- **RTE_NO:** Unknown column
- **ROUTE_TYPE_CODE:** Short values for each county
- **RTE_SUFFIX:** Unknown column 
- **LOG_MILE:** Distance of accident from survey zone
- **LOGMILE_DIR_FLAG_DESC:** Description of direction accident occurred (North, South, West, East) 
- **LOGMILE_DIR_FLAG:** Short term for LOGMILE_DIR_FLAG_DESC
- **MAINROAD_NAME:** Mainroad where the accident occurred
- **DISTANCE:** Distance
- **FEET_MILES_FLAG_DESC:** Description of feet or miles 
- **FEET_MILES_FLAG:** Short term for FEET_MILES_FLAG_DESC (F, M, U) 
- **DISTANCE_DIR_FLAG:** Distance of direction flagged (N, S, E, W) 
- **REFERENCE_NO:** Reference Number 
- **REFERENCE_TYPE_CODE:** Reference number of type code
- **REFERENCE_SUFFIX:** Null Column (unknown) 
- **REFERENCE_ROAD_NAME:** References of road name 
- **LATITUDE:** Latitude of accident 
- **LONGITUDE:** Longtitude of accident
- **LOCATION:** Combination of latitude and longtitude 
- **Counties:** Unknown column 

# Use of Data: 
**Predicting Crashes** 

Crash severity classification: 
- Features:
  - COUNTY_DESC: Counties in Maryland (Montgomery, Frederick, Howard, etc.)
  - YEAR: Values of year the crash occurred 2015-2022
  - QUARTER: Values of each quarter (Q1, Q2, Q3, Q4)
  - COLLISION_TYPE_DESC: Description of collision (Head on righ turn, same direction rear end, etc.)
  - RD_COND_DESC: Description of the road condition (No defects or defects) 
  - RD_DIV_DESC: Description of road divided (Two-way, divided, one-way)
  - LIGHT_DESC: Description of light time (Daylight, Dark, etc.)
  - SURF_COND_DESC: Description of surface condition (Dry, wet, etc.)
  - WEATHER_DESC: Description of weather condition (Blowing sand, clear, raining)
  - HARM_EVENT_DESC1: Description of the cause of accident  
  - HARM_EVENT_DESC2: Description of the cause of accident2
  - REPORT_TYPE: Type of accident reported (Property, fatal, or injury crash)
  - FEET_MILES_FLAG_DESC: Description of feet or miles
  - FIX_OBJ_DESC: Description of property near accident 
  - ACC_DATE: Accident Date
  - ACC_TIME: Accident Time
  - SIGNAL_FLAG_DESC: Yes or No, if direction was flagged 
  - C_M_ZONE_FLAG: Contains values of N or Y 
  - DISTANCE_DIR_FLAG: Distance of direction flagged (N, S, E, W) 
  - JUNCTION_DESC: Description of juntion (Alley, intersection, etc.)
  - LOG_MILE: Distance of accident from survey zone
  - LOGMILE_DIR_FLAG_DESC: Description of direction accident occurred (North, South, West, East)
  - DISTANCE: Distance of the crash
  - REFERENCE_ROAD_NAME: References of road name   

- Target: 
  - REPORT_TYPE: Type of accident reported (Property or Severe crash) 

# Technique and Models: 
Machine Learning Models - **Classification Models:**
- Logistic Regression 
- Random Forest
- Decision Tree 

# Research Question(s): 
Given the data source, there are few questions in my analysis that I would like to address: 
1. What is the number of crashes that occurred for each county?
2. What is the number of crashes for each year? 
3. Does inclement weather condition impact more crashes?
4. What is the county with the most crashes?

# Outcome: 
The goal of this project is to predict the types and severity of crashes in the state of Maryland using ML. Prediction will help audiences understand the nature of accidents that occurred through various types of accidents. 

# References: 
- https://www.richinandgaines.com/blog/2022/09/maryland-ranks-6th-in-the-nation-for-car-crashes/
