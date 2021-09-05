

# SPARKIFY PROJECT
This is the first project from the Data Engineering Nanodegree Program of Udacity.

*Author: Ricardo Miranda*

## Purpose

The purpose of this DB is to consolidate the user and songs played information obtained from the Sparkify app. It consists of 1 fact table of song pays and 4 dimension tables consisting of users in the app, songs in the music DB, artist in the DB and the timestamps of the records.


## Tables Description

### Fact Table

1. **songplays** - records in log data associated with song plays i.e. records with page NextSong
    * *songplay_id*
    * *start_time*
    * *user_id*
    * *level*
    * *song_id*
    * *artist_id*
    * *session_id*
    * *location*
    * *user_agent*

    
### Dimension Tables

1. **users** - users in the app
    * *user_id*
    * *first_name*
    * *last_name*
    * *gender*
    * *level*
1. **songs** - songs in music database
    * *song_id*
    * *title*
    * *artist_id*
    * *year*
    * *duration*
1. **artists** - artists in music database
    * *artist_id*
    * *name*
    * *location*
    * *latitude*
    * *longitude*
1. **time** - timestamps of records in songplays broken down into specific units
    * *start_time*
    * *hour*
    * *day*
    * *week*
    * *month*
    * *year*
    * *weekday*


## Run this code

To run this ETL code do the following:

1. `run create_tables.py`
2. `run etl.py`


## Files in Repository


### sql_queries.py

Contains all the SQL scripts that drop, create, insert and make select queries in the tables.


### create_tables.py

Runs all the SQL scripts that drop and create the tables. Running this file resets the tables, it is used before the ETL scripts. It uses the SQL scripts in *sql_queries.py* as parameters for each querie.


### etl.ipynb

Jupyter Notebook that contains the ETL code explained, state by state for each table. It uses the SQL scripts in *sql_queries.py* as parameters for each querie.


### etl.py

Python file that consolidates the codes in *etl.ipynb* in to one and executes it to fill each table.


### test.ipynb

Jupyter Notebook used to test each table and show if the data was inserted correctly.


