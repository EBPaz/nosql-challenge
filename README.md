# nosql-challenge
 Food Safety Standards - Module 12, July 2023

## About
This project uses Pymongo to gather data from non-SQL databases to be able to gather, manipulate and visualize data. The database in question is a json of food safety evaluations of restaurants in the United Kingdom. This data is being evaluated by ratings and hygiene to aid journalists and food critics on where to focus future articles. The intent is to practice gathering, cleaning and saving data from databases with Mongo.

## Table of Contents
NoSQL_analysis_starter.ipynb -a jupyter Notebook file containing the actual analysis of the gathered data.
NOSQL_setup_starter.ipynb - a Jupyter Notebook file for pulling the data from the json with Pymongo.

## Getting Started / Installation
You will need Mongosh running on your system, then import the dataset with mongoimport with this code:
 --type json -d uk_food -c establishments --drop --jsonArray establishments.json

This project is created and run via Jupyter Notebook or VS Code.

The following imports within your Jupyter Notebook / VS Code are necessary to complete the project:
To gather the data with Pymongo,
from pymongo import MongoClient
from pprint import pprint

To analyze the gathered data for information, include pandas.
import pandas as pd

## Summary 
During the set-up code, I practiced adding new data to the database collection for a specific restaurant by updating data, deleted the entries for the city of Dover and changed data types to reflect the correct form for analysis.

During the specific analysis, 
There are 41 food establishments with a hygiene score of 20 (a very poor hygiene rating).
There are 33 food establishments in London with a 4 or above on the Rating Scale.

When analyzing the 5 food establishments closest to the new restaurant "Penang Flavours", with a rating value of 5(best) and the lowest(best) hygiene scores, each belong to a different business type (ie: Pub/bar vs. Daycare vs. Fast Food)

When analyzing the hygiene scores of 0 (the best hygiene rating) by location, it results in Thanet having the most with 1130 and Tendring the least with 542.

## Acknowledgements
EdEx tutor, Jesse Wright, contributed to the code for building the pipeline to evaluate the closest 5 restaurants with a rating value of 5 and the lowest hygiene score to a new restaurant called, Penang Flavours.

## References
EdEx provided the data resources for this project as follows:

UK Food Standards AgencyLinks to an external site. (2022). UK food hygiene rating data API. https://ratings.food.gov.uk/open-data/en-GBLinks to an external site.. Contains public sector information licensed under the Open Government Licence v3.0Links to an external site.
Accessed Sept 9, 2022 and Sept 12, 2022 with the establishment settings as follows: longitude=51.5072, latitude=-0.1276, maxdistancelimit=4567, pagesize=10000, sortoptionkey=distance, pagenumber=(1,2,3,4,5,6,7,8).
