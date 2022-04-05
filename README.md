# Data Modeling with Postgres

## Summary
***
- [Introduction](#intro)
- [Project Description](#descript)
- [Data](#data)
  - [Data information](#datainfo)
- [Project content](#content)
- [Modeling Cassandra](#model)
  - [DML of Tables](#dml)
- [How to use](#usage)
  - [Requirements](#reg)
  - [Execution](#exec)
- [Conclusion](#conclusion)
***

#### Introduction <a name="intro"></a>

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

They'd like a data engineer to create an Apache Cassandra database which can create queries on song play data to answer the questions The role is to create a database for this analysis. her we are able to test our database by running queries given to you by the analytics team from Sparkify to create the results.


#### Project Description <a name="descript"></a>

In this project, will be applied data modeling with Apache Cassandra and build an ETL pipeline using Python. There are some steps to complete this Udacity Project:
 - *transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.*
 - *model your data by creating tables in Apache Cassandra to run queries.*
 - *Execute queries to check data consistence*
## Data <a name="data"></a>

The dataset is a subset of real data from the Million Song Dataset. The files are partitioned by in CSV by date For example, here are file paths to two files in this dataset.
> \event_data\2018-11-03-events.csv
> \event_data\2018-11-04-events.csv

And below is an example of what the data in a log file, 2018-11-03-events.csv, looks like.
![dataframe sample](https://github.com/Gutelvam/etl_with_cassandra/blob/main/images/image_event_datafile_new.jpg?raw=true "Sample Data")

#### Data information <a name="datainfo"></a>
- **artist** -Artistic name or band
- **firstName** - first name of customer
- **gender** - gender of artist
- **itemInSession** - id of itens in session
- **lastName** - last name of customer
- **length** - Size of song
- **level** - If free or paid
- **location** - City and state
- **sessionId** - id of session
- **song** - name of song
- **userId** - unique id of user

## Project content <a name="content"></a>
There are 2 files  and 2 folders, that are describe below:

- `event_data`: here is the folder containing all  Data in csv format
- `images`: Here is all images used in notebook and Read.me
- `event_datafile_new.csv`: here is a sample of data compressed in a single file.
- `cassandra_pipeline.ipynb`: notebook to build **etl** and **query**  python scripts to solve business problem.


#### **Modeling Cassandra** <a name="model"></a>
The tables used to test and create analytical tables, was modeling to maximize the performance of business queries that is describe below:

![table modeling](https://github.com/Gutelvam/etl_with_cassandra/blob/main/images/table_modeling.png?raw=true "table modeling")

##### **DML of Tables** <a name="dml"></a>
The tables used to test and create analytical tables, was modeling to maximize the performance of business queries that is describe below:


![dml tables](https://github.com/Gutelvam/etl_with_cassandra/blob/main/images/dml_table.png?raw=true "dml tables")

## How to  use <a name="usage"></a>
The DML for tables are descripted below:

#### Requirements <a name="reg"></a>
     - numpy==1.16.2
     - pandas==0.24.2
     - cassandra-driver >= 3.2
#### Execution <a name="exec"></a>
 
For this step first you must to clone all repository and execute in that order and be sure to install all requirements, start jupyter notebook in the folder and open  `cassandra_pipeline.ipynb`.

After that you may execute the `.ipynb` file to Check solution.

## Conclusion <a name="conclusion"></a>
In this project we have modeled  and created Analytical tables for query optimization in Cassandra DB, in this process we applied the most common data engineering process: Extract, transform and load by inserting transformed data into the business significant tables that can be used in the analysis process.
