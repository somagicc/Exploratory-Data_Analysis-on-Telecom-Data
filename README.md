# Exploratory Data Analysis on Telecom Data
## Introduction
As part of Capstone project, I worked on the studying the demographics (gender and age) of users of InsaidTelecom based on their usage behaviours to provide actionable insights for impactful offerings by the company. Our analysis is restricted to users of the following states:
- MadhyaPradesh 
- Chhattisgarh
- Uttaranchal
- Jammu and Kashmir 
- Goa
- Nagaland  

## Project Description
InsaidTelecom, one of the leading telecom players, understands that customizing offering is very important for its business to stay competitive.
Currently, InsaidTelecom is seeking to leverage behavioral data from more than 60% of the 50 million mobile devices active daily in India to help its clients better understand and interact with their audiences.
In this consulting assignment, we are analysing the data to understand user's demographic characteristics based on their mobile usage, geolocation, and mobile device properties.
Doing so will help millions of developers and brand advertisers around the world pursue data-driven marketing efforts which are relevant to their users and catered to their preferences.

## Problem Statement
Suggest actionable insights to help the company design its offering based on user behaviour and demographics.

## Sources of Data
|   Table Name | Description/ Name of Columns  |
| ------------ | ------------ |
| gender_age_train  | device ids , gender , age,  age group   |
| phone_brand_device_model  | device ids, brand, models, phone_brand |
| events_data | When a user uses mobile on INSAID Telecom network, the event gets logged in this data. Each event has an event id, location (lat/long), and the event corresponds to frequency of mobile usage. timestamp (when the user is using the mobile) |

## Problem Analysis
We divided the broad goal into following smaller goals:
1.	Distribution of Users(device_id) across States
2.	Distribution of Users across Phone Brands
3.	Distribution of Users across Gender
4.	Distribution of Users across Age Segments
5.	Distribution of Phone Brands for each Age Segment, State, Gender.
6.	Distribution of Gender for each State, Age Segment and Phone Brand
7.	Distribution of Age Segments for each State, Gender and Phone Brand
Note: We are considering 10 most used phone brands for analysis.

Collating the above points, we have built actionable insights for the company.

## Major Data Mining Steps
|  Issue | Resolution   |
| ------------ | ------------ |
| In events_data, device_id had 51 null values | It was observed that corresponding to 3 latitude and longitude values we have missing device_id values (17 each). So, these null values were filled using the corresponding latitudes and longitudes values.|
| In events_data, longitude and lagitude had 63 null values each  | It was observed that the same device_id values had missing longitude and latitude values. Corresponding to 3 device ids, we have latitude and longitude values (21 each). So, these null values were filled using the corresponding device ids.  |
| In phone_brand_device_model, Out of 60 phone brands, 52 are in Chinese. Out of 676 models, 92 are in chinese. | Translated using the Chinese to English mapping information present in the dataset description and Google translate package. |
| In phone_brand_device_model, Many of them are a combination of chinese and English names like '红米Note2', '联想黄金斗士S8' which cannot be replaced using the method used for phone brand column. These are new values like '联想黄金斗士S8' is 'Lenovo Gold Fighter S8' | Translated the values from English to Chinese using google translator python package |
| In the three tables, device_id is the common field to combine data from all the tables.  | All three tables were merged on device id |
## Major Insights
1. The most popular brands are shown below.

2. The most popular device models are shown below.

3. Mobile brands preferred by Male are shown below.

4. Mobile brands preferred by Female are shown below-

5. The most popular brands for various age groups are shown below.

## Tools Used
- Jupyter notebooks
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Folium
- Google translation APIs

## Actionable Insights
●	New plans can be introduced based on the different age groups,locations and their usage, like plans for data and plans for talktime based on the usage patterns.
●	New plans can be based on the customer diversity, like for students, housewives and corporate employees have different requirements and usages, so can provide customized plans to them.
●	Possibility to introduce combo plans consisting of attractive monthly or quarterly  plans along with the top brands of mobiles, so that users can opt for the mobile devices of their choice with flexible payment options.
●	Signal strength needs to be monitored and maintained in peak hours so that users should not face issues and promote the company to other future potential customers.
●	Plan for more marketing campaigns in the areas with less customers to increase the customer base and can introduce some introductory offers for new customers in those areas.

Find detailed consulting report here.
You can find presentation of analysis on data here.

