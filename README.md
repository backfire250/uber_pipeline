# Data Engineering with Uber: Project Overview
**Project Goal**:  Collect relevant data from thousands of Uber trips and create a dashboard to visualize my findings.
* Create a data pipeline to automate data cleaning and send cleaned data to a dashboard.
* Store data in Google Cloud and create a virtual machine to perform data cleaning and analysis.
* Collect data from 10,000 Uber trips in New York. 
* Map out data transformations in Lucid Charts.
* Create a simple dashboard in Looker Studio.

## Project Steps
1. Project Planning
2. Data Collection
3. Data Cleaning
4. Exploratory Data Analysis
5. Data Pipeline Creation
6. Dashboard Creation

## Code and Resources Used  
**Python Version:** 3.7   
**Packages:** pandas, numpy 
**Looker Studio:** Used to create a simple dashboard after the data had been cleaned and the data pipeline had been built.
**Jupyter Notebooks:** Used to run code in Python for data cleaning and data analysis.
**BigQuery API:** API creation to send data.
**Lucid Charts:** Mapped out how I wanted to transform the data from what I collected into something I could use for data analysis.
**Google Cloud Console:** Used to store the data for my project.
**Google Compute Engine:** Created a virtual machine.
**Anaconda:** Collection of Python tools specifically tailored for Data Science projects.

## YouTube Project Walk-Through
For this project, I followed the below YouTube video series to familiarize myself with some data science tools:
https://www.youtube.com/watch?v=WpQECq5Hx9g

## Data Collection and Modeling
After collecting the data, I needed to map everything out to decide which tables and columns I was going to keep and which tables and columns I would need to create. I found it would be easier to break down the collected data into specific groups and create smaller tables. Below is an example of how I restructured the data:
![](https://github.com/backfire250/uber_pipeline/blob/main/lucid_chart.png)

## Data Cleaning
I needed to clean up the data so that it would be consistent and usable for data analysis. I made the following changes and created the following tables:

*	Created a datetime table where all of the pickup/dropoff times are stored.
*	Created tables for pickup location and dropoff location that stored latitude and longitude.
*	Mapped out payment types to analyze how customers were paying for trips.
*	Mapped out rate codes to show the different types of rates customers were being charged.
*	Created a trip distance table to track the distance of each Uber trip.
*	Created a passenger count table to keep track of how many passengers were on each trip.
*	Created a final "fact table" that had only the relevant columns needed for data analysis.

## EDA (Exploratory Data Analysis)
* I started by creating some histograms to look at some of the more relevant columns such as trip fare, rate code, and payment type.
* I also wanted to look at the number of passengers per ride and see if that correlated with trip distance.
* Looked at which data points correlated well and which ones didn't.
* Set up pivot tables to drill down into the data.

## Data Pipeline Creation
* In this step, I built a data pipeline using Mage AI to automate my entire process for future use.
* The pipeline automatically collected new data, cleaned it using the code I wrote in the "Data Cleaning" step, and sent the cleaned data to a location where it could be viewed in a dashboard.

## Dashboard Creation
I created a simple dashboard here:
* Using the tables I created for pickup and dropoff location, I was able to heatmap all of the various Uber trips and break them down by rate code and payment type.
* I also created several graphs breaking down the average fare by rate code and payment type.
* I then provided some general highlights from the data such as: average fare amount, average tip amount, average trip distance, and total number of Uber trips.
![](https://github.com/backfire250/uber_pipeline/blob/main/dashboard_screenshot.png)
