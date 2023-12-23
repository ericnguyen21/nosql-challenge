# nosql-challenge
Module 12 Challenge

Goal
The goal of the project is to evaluate food hygiene ratings of establishments across the UK, to assist the journalists and food critics of the food magazine "Eat Safe, Love" in identifying where to focus future articles.

Repository Structure
Source code:

NoSQL_setup.ipynb contains the code to setup the database for analysis.
NoSQL_analysis.ipynb contains the analysis code.
The Resources directory contains the dataset: establishments.json

Dataset
UK Food Standards Agency Links to an external site (2022). Available from: https://www.food.gov.uk/

UK food hygiene rating data API. Available from: https://ratings.food.gov.uk/open-data/en-GB

Approach
Import the database using the following code:

mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json

Confirm the database and its collections were correctly created.

Check the database: list_database_names()
Check the collections: list_collection_names()
Confirm the documents exist: establishments.find_one()

Update the database as per the food magazine's requirements:

Add a document for a new, unrated restaurant: Penang Flavours.
Remove all establishments in Dover.
Clean the data by converting to the correct datatypes.

Analysis

- Which establishments have a hygiene score equal to 20?
There are a total of 41 establishments that meet the criteria of having a hygiene score equal to 20. You can find the details and names of these establishments in the NoSQL_analysis.ipynb notebook.

- Which establishments in London have a RatingValue greater than or equal to 4?
A total of 33 establishments in London meet the criteria of having a RatingValue greater than or equal to 4. For specific names and details, you can refer to the NoSQL_analysis.ipynb notebook.

- What are the top 5 establishments with a RatingValue rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added Penang Flavours?
Howe and Co Fish and Chips - Van 17
Atlantic Fish Bar
Plumstead Manor Nursery
Iceland
Volunteer

- How many establishments in each Local Authority area have a hygiene score of 0?
There are a total of 55 local authorities where at least one establishment has a hygiene score of 0. If you want a breakdown of the count for each local authority, please check the NoSQL_analysis.ipynb notebook.
