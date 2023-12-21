## NoSQL Challenge: UK Food Standards Agency Data Analysis

Project Overview

This project, commissioned by "Eat Safe, Love" magazine, involves analyzing food hygiene ratings from the UK Food Standards Agency. The goal is to assist journalists and food critics in focusing their articles on establishments based on their hygiene ratings. The project is divided into three parts: setting up the database and Jupyter Notebook, updating the database, and performing exploratory analysis.

Part 1: Database and Jupyter Notebook Setup

Steps:
- Import necessary libraries: PyMongo and Pretty Print (pprint)
- Establish a connection to the MongoDB instance using the Mongo Client.
- Import the establishments.json database file in terminal.
## mongoimport --db uk_food --collection establishments --jsonArray --file establishments.json
- Verify the successful creation of the database and the collection.


Part 2: Update the Database

Objectives:
Add New Restaurant: Insert a new restaurant "Penang Flavours" into the establishments collection.
Update Business Type ID: Locate and update the BusinessTypeID for "Restaurant/Cafe/Canteen".
Remove Establishments in Dover: Identify and delete establishments associated with the Dover Local Authority.
Data Type Conversion: Convert latitude, longitude, and RatingValue to appropriate numeric types using update_many.
Implementation:
MongoDB queries and update operations to modify the database as per the magazine's requirements.

Part 3: Exploratory Analysis

Analysis Goals:
- Hygiene Score Analysis: Identify establishments with a hygiene score of 20.
- High-Rated London Establishments: Find establishments in London with a RatingValue of 4 or higher.
- Top Establishments Near Penang Flavours: Determine the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, and close to "Penang Flavours".
- Analyze the distribution of establishments with a hygiene score of 0 across different Local Authority areas.

Methodology:
Each analysis point involves querying the MongoDB database using PyMongo.
Results are counted, displayed, and converted to Pandas DataFrames for further examination.
Sorting, grouping, and aggregation are employed to derive meaningful insights.


Conclusion

This project demonstrates a comprehensive application of NoSQL databases (MongoDB) for data analysis, combined with Python scripting (PyMongo and Pandas) to extract, process, and present data-driven insights. The findings from this project will guide "Eat Safe, Love" in highlighting establishments based on their food hygiene ratings.
