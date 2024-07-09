# sqlalchemy-challenge
homework for Module 10-SQLalchemy

In this section, we used Python and SQLAlchemy to do a basic climate analysis and data exploration of our climate database. Specifically, we used SQLAlchemy ORM queries, Pandas, and Matplotlib. 


- We  provided with  files (climate_starter.ipynb and hawaii.sqlite) to complete  climate analysis and data exploration.

- We used the SQLAlchemy create_engine() function to connect to our SQLite database.

- We used the SQLAlchemy automap_base() function to reflect our tables into classes, and then saved references to the classes named station and measurement.

- We Linked Python to the database by creating a SQLAlchemy session.

- We Perform a precipitation analysis and then a station analysis


Precipitation Analysis:


- Using that date, we got the previous 12 months of precipitation data by querying the previous 12 months of data.
- Selected only the "date" and "prcp" values.

- Loaded the query results into a Pandas DataFrame. Explicitly set the column names.

- Sorted the DataFrame values by "date".

- Plot the results by using the DataFrame plot method
- Used Pandas to print the summary statistics for the precipitation data.


Station Analysis:


- Design a query to calculate the total number of stations in the dataset.

- Design a query to find the most-active stations (that is, the stations that have the most rows). To do so, complete the following steps:

- Listed the stations and observation counts in descending order.

- Designed a query that calculates the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.

- Answerd the following question: which station id has the greatest number of observations?


- Designed a query to get the previous 12 months of temperature observation (TOBS) data. To do so, complete the following steps:

- Filtered by the station that has the greatest number of observations.

- Query the previous 12 months of TOBS data for that station.

- Plot the results as a histogram with bins=12


Part 2: Designed  Climate App


We designed a Flask API based on the queries that  developed.

- Started at the homepage.

- Listed all the available routes. /api/v1.0/precipitation

- Converted the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value.

- Returned the JSON representation of  dictionary. /api/v1.0/stations

- Returned a JSON list of stations from the dataset./api/v1.0/tobs

- Query the dates and temperature observations of the most-active station for the previous year of data.

- Returned a JSON list of temperature observations for the previous year.

/api/v1.0/<start> and /api/v1.0/<start>/<end>

- Returned a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.

- For a specified start, calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.

- For a specified start date and end date, calculate TMIN, TAVG, and TMAX for the dates from the start date to the end date, inclusive.




