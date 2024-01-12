# ROAD ACCIDENT ANALYSIS - POWER BI 2023
## Introduction to Road Accident Analysis for Power BI Project:

Road accidents pose a significant threat to public safety and result in numerous fatalities and injuries worldwide. Analyzing road accident data is crucial for understanding the contributing factors, identifying patterns, and implementing effective measures to improve road safety. Power BI, a powerful business intelligence tool, can be employed to visually explore and communicate insights derived from road accident data.

**Objective:**
The primary goal of the Road Accident Analysis Power BI project is to leverage data visualization techniques to gain a comprehensive understanding of road accidents, their causes, and potential preventive measures. By using Power BI, we can transform raw data into actionable insights, empowering decision-makers, law enforcement agencies, and policymakers to make informed choices and enhance road safety.

**Data Sources:**
Road Accident Data.xlsx

## Tools Used
POWER BI

**Key Components of Analysis:**

1. **Spatial Analysis:**
   - Geospatial mapping to identify accident hotspots.
   - Visualization of accident clusters and their correlation with specific geographic features.

2. **Temporal Analysis:**
   - Time series analysis to identify trends and patterns in accident occurrences.
   - Monthly, breakdowns to understand peak accident periods.

3. **Causal Factors:**
   - Identification and visualization of key contributing factors such as speeding, impaired driving, weather conditions, and road types.
   - Correlation analysis to determine relationships between variables.

4. **Demographic Insights:**
   - Analysis of accidents based on vehicle type.

5. **Impact Analysis:**
   - Visualization of the severity of accidents.

**Power BI Features Utilized:**

1. **Data Transformation:**
   - Cleaning and preprocessing raw data to create a clean and structured dataset.

2. **Data Modeling:**
   - Building relationships between various data tables for comprehensive analysis.

3. **Data Visualization:**
   - Creation of interactive dashboards and reports to present insights effectively.
   - Implementation of custom visuals to enhance storytelling.

4. **Predictive Analytics (Optional):**
   - Integration of predictive models to forecast potential accident hotspots or identify high-risk areas.

By combining the analytical capabilities of Power BI with comprehensive road accident data, this project seeks to contribute to the ongoing efforts to enhance road safety and mitigate the impact of accidents on society.
This project delves deep into the realm of data analysis, utilizing SQL and Power BI to uncover crucial insights into Pizza sales. The featured eye-catching dashboards aid the pizza business in making informed decisions and strategic workforce planning, providing substantial benefits to the business.

## STEPS IN PROJECT
1.Requirement Gathering
2.Stakeholders in project
3.Raw Data Overview
4.Connecting Data with POWER BI
5.Data Cleaning
6.Data Processing
7.Data Modelling
8.Data Visualization/ Charts Design
9.Reports/ Dashboard Building
10.Insights

## PROBLEM STATEMENT
To create a Road Accident Dashboard for year 2021 and 2022 so that they can have insight on the below requirements,
1. Primary KPI - Total Causalities and Total Accident Values for Current Year and YOY Growth
2. Primary KPI's - Total Causalities by Accident Severity for Current Year and YOY Growth
3. Second KPI'S - Total Casuality with respect to Vehicle type for Current Year
4. Monthly trend showing comparision of casualities for current year and previous year
5. Casualities by Road Type for current year
6. Current Year Casualities by Area/Location and by Day/Night
7. Total casualities and Total Accidieents by Location

## STAKEHOLDERS
1. Ministry of Transport
2. Road Transport Department
3. Police Force
4. Emergency Services Department
5. Road Safety Corps
6. Transport Operators
7. Traffic Management Agencies
8. Public
9. Media

## POWER BI FUNCTIONALITIES
1. How to connect to raw/flat file
2. Data Cleaning in Power Query
3. Data Processing
4. Time Intelligence Function/ Calendar Date Table in POWER BI
5. Data Modelling (Relationship between multiple tables)
6. YTD and YOY Growth Calculations Using DAX
7. KPI and Advanced KPI Generations
8. Creating Custom columns and measure in the reports
9. Importing images
10. Creating different charts and Generating Insights
11. Export the report to users

## CONNECTING TO DATA SOURCE
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/e50ff6e8-0cf1-4bab-ba23-c29839ecdc68)

## LOAD THE DATA
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/8083adae-1a0e-46f7-a265-3fc52633b6c5)


## DATA CLEANING
Now select the Entire Accident Severity column, replace the Fetal name in the Accident Severity with Fatal name
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/8cdbf9f8-69e0-4286-9b48-f6077bbc1569)

## DATA MODELLING
CREATING DATE TABLE
1. To Determinne the Year to Date Casualities
2. Year on Year Casualities
In this case we have to use Time Intelligence Function
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/0f66d0f2-51af-45b6-94c5-27fabee79aa4)

## BUILDING RELATIONSHIP (ONE TO MANY RELATIONSHIP)
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/4bc016bf-3a7b-41da-8cba-ff128ff44209)

## MEASURES USED
## CY Casualities = TOTALYTD(SUM(Data[Number_of_Casualties]),'Calendar'[Date])
![Screenshot (158)](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/31e767ee-d448-4dd7-89ed-4eee981184e9)

## CY Accidents = TOTALYTD(COUNT(Data[Accident_Index]),'Calendar'[Date])
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/583bec5f-41af-468d-a9d5-98e5470546e2)

## PY Casualities = CALCULATE(SUM(Data[Number_of_Casualties]),SAMEPERIODLASTYEAR('Calendar'[Date]))
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/f73b637f-0a84-4970-995f-7b4dfeb7046d)


## PV Accidents = CALCULATE(COUNT(Data[Accident_Index]),SAMEPERIODLASTYEAR('Calendar'[Date]))
![Screenshot (161)](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/612a5030-af11-44be-bf93-09d1eceacf51)


## YOY Casualities = ([CY Casualities]-[PY Casualities])/[PY Casualities]
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/6b93aec1-58a5-47b3-b718-de8630226b84)


## YOY Accidents = ([CY Accidents]-[PV Accidents])/[PV Accidents]
![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/36278f56-7c74-4a6a-b668-d9b138850cd3)


## DASHBOARD CREATION
Total Current Year Casualities

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/f01ff136-1f19-41e0-8ffb-650a4843ffc5)

## Total Current Year Accidents

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/7db7dde6-70c5-4f68-a39e-be308c5d432a)

## Current Year Fatal Casualities

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/8e4e4e7e-4603-4419-ac93-a77cabc95ccc)

## Current Year Serious Casualities

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/907e3eed-03b3-48e6-a1a0-d602d2f41010)

## Current Year Slight Casualities

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/8a01c8b6-87c0-4e8a-abf8-606edbeb8261)

## Current Year Casuality Vs Previous Year Casuality Monthly Trend

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/91f2e1c0-1185-4159-9898-c56549080fca)

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/173a6a41-ca78-448e-bb4d-e5e0f143f0b4)

## CY Casualities by Urban_or_Rural_Area

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/aa671bcb-d5fe-406a-a4b6-58426a0a1118)

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/9e252b7c-e8f6-4de5-ab05-6d78dd654e4d)

## Casualities by Road_Type

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/42c83580-621b-4c01-88a4-3d9f4475c977)

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/0fd9b0ff-6e4d-4b45-8cdd-4f7e697ad72c)


## Casualities by Light_Conditions 

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/4abd593e-00d2-49c9-821e-753b73861c7b)

![image](https://github.com/PRATHAMESH9743/ROAD-ACCIDENT-ANALYSIS/assets/154798147/9d6cf9ce-e40c-4188-9e88-98f0e0a768fe)

