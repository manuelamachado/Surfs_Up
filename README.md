# Surfs Up!

Used SqlAlchemy to create a database to store weather inforamtion in Honolulu, Hawaii;
Queried the data from database, analyzed the data by PANDAS and offered visualization using matplotlib

Step1. Data Cleaning and database engineering

* Input: Two csv files with Hawaii weather and station information in the directory /Resources
* Script: Used Pandas and SQLAlchemy to clean data and create database to store the data
* Output: Two cleaned csv files and hawaii.sqlite stored in the output directory

Step2. Data retrieving, analysis and visualization

* Input: Retreieved data from the database created at Step1
* Output: Data Visualizations stored in the output directory


## Step 1 - Data Engineering

* Created a Jupyter Notebook file called `data_engineering.ipynb` and use this to complete all of my Data Engineering tasks.

* Used Pandas to read in the measurement and station CSV files as DataFrames.

* Inspected the data for NaNs and missing values. Decided what to do with this data.

* Saved my cleaned CSV files with the prefix `clean_`.

---

## Step 2 - Database Engineering

* Created a Jupyter Notebook called `database_engineering.ipynb` and use this to complete all of my Database Engineering work.

* Used Pandas to read my cleaned measurements and stations CSV data.

* Used the `engine` and connection string to create a database called `hawaii.sqlite`.

* Used `declarative_base` and created ORM classes for each table.

* Created the tables in the database using `create_all`.

---

## Step 3 - Climate Analysis and Exploration

Analysis completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.

* Created a Jupyter Notebook file called `climate_analysis.ipynb` and use it to complete my climate analysis and data exporation.

* Chose a start date and end date for my trip.

* Used SQLAlchemy `create_engine` to connect to my sqlite database.

* Used SQLAlchemy `automap_base()` to reflect my tables into classes and save a reference to those classes called `Station` and `Measurement`.

### Precipitation Analysis

* Designed a query to retrieve the last 12 months of precipitation data.

* Selected only the `date` and `prcp` values.

* Loaded the query results into a Pandas DataFrame and set the index to the date column.

* Plotted the results using the DataFrame `plot` method.

* Used Pandas to print the summary statistics for the precipitation data.

### Station Analysis

* Designed a query to calculate the total number of stations.

* Designed a query to find the most active stations.

* Listed the stations and observation counts in descending order.

* Identified which station has the highest number of observations.

* Designed a query to retrieve the last 12 months of temperature observation data (tobs).

  * Filtered by the station with the highest number of observations.

  * Plotted the results as a histogram with `bins=12`.

### Temperature Analysis

* Wrote a function called `calc_temps` that accepts a start date and end date in the format `%Y-%m-%d` and return the minimum, average, and maximum temperatures for that range of dates.

* Used the `calc_temps` function to calculate the min, avg, and max temperatures for my trip using the matching dates from the previous year.

* Plotted the min, avg, and max temperature from my previous query as a bar chart.

  * Used the average temperature as the bar height.

  * Used the peak-to-peak (tmax-tmin) value as the y error bar (yerr).


