# Movies-ETL

# Purpose 

The purpose of this project is to use the data pipeline process of ETL (Extract, Transform, and Load) to collect, import, and process data. Python and Pandas was used to perfrom data wrangling and PostgreSQL was used store the finished data. 

* Creating an ETL pipeline from raw data to an SQL database
* Extracting data from disparate sources with Python
* Cleaning and transforming data from a JSON file using Pandas
* Using regular expressions to parse data and transform text into numbers
* Loading the data into PostgreSQL 

# Summary

Initial project: 

Raw data was gathered from Wikipedia and Kaggle and extracted from thier respective files. Both datasets were were cleaned and joined together during the transformation step. The goal of the transformation step is to create a consistent structure in the data. Once the structure of the data was consistent, the cleaned dataset was loaded into a relational database. 


Challenge: 

After the initial project was completed, a new automated pipeline was created. The new pipeline takes in new data, performs the appropriate transformations, and uploads the new data into the existing tables. This was accomplished by refactoring the code from the initial project. The refectored code utilizes a single function gather data from three sources, perform the ETL process, and upload the data into our database on PostgreSQL. 

The challenge consisted of four deliverables:

1. Write an ETL Function to read three data files and create three separate dataframes.

A single ETL function reads in three data files. The function converts the Wikipedia JSON file, the Kaggle metadata, and the MovieLens ratingsdata CSV file each into thier own Pandas dataframe. 

2. Extract and transform the Wikipedia data

The Wikipedia data was extracted and transformed to be merged with the Kaggle metadata. A regular expression string was used to extract IMDb ID's and drop duplicates. A try-except block was introduced to find errors. 

3. Extract and transform the Kaggle data

The Kaggle metadata and the MovieLens rating data were seperately extracted and transformed to the same consistent structure as the Wikipedia data. The transformed Kaggle dataset was converted into a dataframe, and the transformed MovieLens rating data was converted into a seperate dataframe. Then, the Kaggle dataframe was merged with the Wikipedia dataframe from the previous deliverable to create the movies_df. Movies_df was then merged with the MovieLens rating dataframe to create a dataframe that contains movies with thier respective ratings. 

4. Create the Movie database

The movies_df dataframe and the MovieLens rating CSV files were added to an SQL database. Queries were performed to confirm successful completion of this step. Images of these quesies have been provided. 
