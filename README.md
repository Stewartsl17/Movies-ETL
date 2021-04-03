# Movies - ETL 

## Project Overview

For this project, we were asked to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. In order to do this, we had to refactor our code to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

### Resources 

* Software: Jupyter Notebooks and SQL

## Results

First, we defined a function to read in our three data files and creates three separate DataFrames. Here is our function: 

![](https://github.com/Stewartsl17/Movies-ETL/blob/master/Images/ETL%20Function.png)

Based on the above function, we have pulled the three data files into our code. We have a DataFrame for each of our datafiles. First, we have the Wiki Movies dataframe: 

* Table: Wiki Movies dataframe
![](https://github.com/Stewartsl17/Movies-ETL/blob/master/Images/Wiki%20Movies%20Dataframe.png)

Next, we have the metadata that we pulled from Kaggle and converted into a dataframe: 

* Table: Kaggle Movies dataframe
![](https://github.com/Stewartsl17/Movies-ETL/blob/master/Images/Kaggle%20Movies%20Dataframe.png)

Finally, we have the ratings data that we converted into a dataframe:

* Table: MovieLens Ratings dataframe <br>
![](https://github.com/Stewartsl17/Movies-ETL/blob/master/Images/Ratings%20Dataframe.png)

Once our data was read in, we were to extract and transform the Wiki data in order to merge it with the Kaggle dataset, which was done [here](https://github.com/Stewartsl17/Movies-ETL/blob/master/ETL_clean_wiki_movies.ipynb). Then, we used the same process to combine those two datasets with the MovieLens rating data [here](https://github.com/Stewartsl17/Movies-ETL/blob/master/ETL_clean_kaggle_data.ipynb)

After merging our three files, we then needed to create a database in SQL in order to query the data for movies and ratings. Here is a query for ratings: 

* Table: Ratings Query <br>
![](https://github.com/Stewartsl17/Movies-ETL/blob/master/ratings_query.png)

* Table: Movies Query <br>
![](https://github.com/Stewartsl17/Movies-ETL/blob/master/movies_query.png)
