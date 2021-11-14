# Movies-ETL
## Overview
For this project, we are setting up an automated pipeline that takes in new data from Wikipedia's Movie Data, Kaggle's Metadata, and MovieLens' ratings data. I setup an Extract, Transform, and Load(ETL) function so when new data is added, our code performs the necessary transformations and loads the data into the existing PostgreSQL database so we are woking with the most up to date movie information. I created this pipeline by splitting the task into 4 sections: 
- Write an ETL Function to read the three data files
- Extract and transform the Wikipedia Data
- Extract and transform the Kaggle and Ratings Data
- Load the cleaned and transformed data into a PostgreSQL DataBase
## Results
### Write an ETL Function to read the three data files
This function takes the Wikipedia JSON, the Kaggle metadata and the MovieLens CSV files and creates three DataFrames for each of these datasets
### Extract and transform the Wikipedia Data
This function consolidates redundant data, adding missing data for relevant columns, filtering out TV Shows and formatting each DataFrame to have matching columns
### Extract and Transform the Kaggle and Rating Data
This function follows a similar path as the Wikipedia data. I consolidated the redundant data, removed the duplicates, added missing data for relevant columns, and formatted the data to match that of the Wikipedia data. I then merged the Kaggle and Rating Data with the Wikipedia movies DataFrame.
### Load the cleaned and transformed Data into a PostgreSQL DataBase
This step moves the cleaned and transformed data from Python and Pandas into a PostgreSQL DataBase. As more data gets added to Wikipedia movies, Kaggle Metadata, and the Ratings file it can now easily be added to the PostgreSQL Database:
![This is an image](https://github.com/weise142/Movies-ETL/blob/main/PostgreSQL%20movies.png)
## Summary
This ETL function collects, cleans, and transforms movie data from different sources and in different formats. Once the data is cleaned and transformed, it then merges the information into one DataFrame and exports it to the PostgreSQL Movies data table so the most up to date information can be used by the Amazing Prime Hackathon participants so novel analysis can be performed and Amazing Prime can make better informed business decisions.
