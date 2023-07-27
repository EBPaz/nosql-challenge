# nosql-challenge
 Food Safety Standards - Module 12, July 2023

##About
This project uses Pymongo to gather data from non-SQL databases to be able to gather, manipulate and visualize data. The database in question is a json of food safety evaluations of restaurants in the United Kingdom. This data is being evaluated by ratings and hygiene to aid journalists and food critics on where to focus future articles. 

##Table of Contents
NoSQL_analysis_starter.ipynb -a jupyter Notebook file containing the actual analysis of the gathered data.
NOSQL_setup_starter.ipynb - a Jupyter Notebook file for pulling the data from the json with Pymongo.

##Getting Started / Installation
This project is created and run via Jupyter Notebook.

The following imports are necessary to complete the project:
To gather the data with Pymongo,
from pymongo import MongoClient
from pprint import pprint

To analyze the gathered data for information, include pandas.
import pandas as pd


##Acknowledgements
EdEx tutor, Jesse Wright, contributed to the code for building the pipeline to evaluate the closest 5 restaurants with a rating value of 5 and the lowest hygiene score to a new restaurant called, Penang Flavours.