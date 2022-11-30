# Data lake in AWS

Introduction - The purpose of the project, What is Sparkify, how this project is going to help it.
Database schema design and ETL process
Files in repository
How to run the python scripts
Properly use the markdown syntax in your README, for headings, lists, subsections. Refer: https://guides.github.com/features/mastering-markdown/
You can use an online markdown editor like https://dillinger.io/


## Introduction
A music streaming startup, Sparkify, has grown their user base and song database even more and want to move their data warehouse to a data lake. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

As their data engineer, you are tasked with building an ETL pipeline that extracts their data from S3, processes them using Spark, and loads the data back into S3 as a set of dimensional tables. This will allow their analytics team to continue finding insights in what songs their users are listening to.

You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare your results with their expected results.


## Database Schema

songs_table

![image](https://user-images.githubusercontent.com/65776444/204892733-ef229b66-26a8-4973-84cf-27688cce2529.png)

artists_table

![image](https://user-images.githubusercontent.com/65776444/204892840-9a3ccddb-e620-4ffd-bcd1-45d3d357a47e.png)

user_table

![image](https://user-images.githubusercontent.com/65776444/204892914-aeb5951b-f856-434e-8afd-94f5e05ecbc7.png)


time_table

![image](https://user-images.githubusercontent.com/65776444/204893003-c885c094-f90b-414e-a4d3-1b7e8c501ce9.png)

songplay_table

![image](https://user-images.githubusercontent.com/65776444/204893331-5d4d37bf-3d0c-4808-b70f-0dcbf433963e.png)


## files in project

### dl.cfg
configuration file where youmust include zour own AWS credentials.

![image](https://user-images.githubusercontent.com/65776444/204895168-f803a00d-190c-4ee0-ba78-31615ef4c323.png)


### etl.py
python script where the S3 buckets are read and write the parquet files in another bucket.


### sparkses.ipynb
Jupyter Notebook where most of process was runned before etl.py was assembled. 


## How to run

- create a bucket in S3 where the output must be saved.
- Run python etl.py
