# Google-Data-Analytics-Certificate-Capstone-Project
## Cyclistic bike-share analysis case study

### Introduction:
I will follow the data analysis process which I learned from the course:

1. Ask: business challenge, objective, or question
2. Prepare: data generation, collection, storage, and data management
3. Process: data cleaning and data integrity
4. Analyze: data exploration, visualization, and analysis
5. Share: communicating and interpreting results
6. Act: putting  insights to work to solve the problem

Cyclistic is a bike-share company with a fleet of 5,824 bicycles and 692 stations across the city. Customers can rent bikes from one station and return them to any other station within the network at their convenience.

Cyclistic's marketing strategy has so far focused on building general awareness and appealing to broad consumer segments. They offer flexibile pricing plans single-ride passes, full-day passes, and annual memberships. Besides, it provides reclining bikes, hand tricycles, and cargo bikes, effectively welcoming individuals with disabilities and those who can't ride on the standard two-wheeled bicycles. 
Based on the company database, Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day. While traditional bikes remain as the popular option, around 8% of users opt for the assistive alternatives.

The company's marketing director believes that the company’s future success depends on maximizing the number of annual memberships. Therefore, I have to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, we will design a new marketing strategy to convert casual riders into annual members.

### ASK
Case Study Roadmap - Ask
Guiding questions
    1.  What is the problem you are trying to solve? Design marketing strategies aimed at converting casual riders into annual members
    2. How can your insights drive business decisions?
        - How do annual members and casual riders use Cyclistic bikes differently?
        - Why would casual riders buy Cyclistic annual memberships?
        - How can Cyclistic use digital mediat to influence casual riders to become members?
 
Key tasks
  - Identify the business task: To understand how casual riders behave differently from riders with paid memberships
  - Consider key stakeholders: Director of Marketing (Lily Moreno), Cyclists Executive team, Cyclistic Marketing Analytics team
 
Deliverable
  - A clear statement of the business task

### PREPARE
**Data Source**

I used the previous 12 months of Cyclistic drip data to analyze and identify trends. This data was obtained through the [divvy_tripdata](https://divvy-tripdata.s3.amazonaws.com/index.html) source. The data has been made available by Motivate International Inc. under this license.

![image](https://github.com/user-attachments/assets/0b7739fb-74e8-4b39-98cf-abfa3392e3c4)

- Data Timeframe: May 2024 to April 2025 (past 1 year data)
- The data is organized into individual .csv files, each corresponding to a specific month. The files share common fields relevant to analysis.
- After initial examination, source data is Reliable, Original, Comprehensive, Current, Cited.

**Tool Selection for Analysis** 
- Excel used for Data Cleaning, Trasformation and Processing
- Tool for Analysis and Visualization: Excel Pivot Tables

### PROCESS
**Data Cleaning and Transformation Process**
To merge, explore and clean the data I opted for Microsoft Excel and Power Query

1. Activated filters for each column and reviewed blank spaces, duplicates and inconsistencies of the dataset
2. Uploaded all 12 .csv datasets to PowerQuery
3. Removed columns
   - ride_id, start_lat, start_lng, start_lat, end_lng as it was irrelevant to identifying behavioural trends
   - start_station_name, start_station_id, end_station_name, end_station_id as the objective is not to market to stations but rather people
4. New columns "Month" "Day Name" "Hour" added from the "started_at" column
5. Custom column "Ride Time" in minute format added using the formula '=([ended_at]-[started_at])*24*60'
6. Conditional column added to categorise Ride Time for easier analysis
   ![image](https://github.com/user-attachments/assets/42d99d8c-3ee4-4084-aea3-c31aaef31612)
7. "Ride Time", "started_at", "ended_at" column removed.
8. Load data into Excel for data visualisation

### ANALYSE
