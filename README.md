# sqlalchemy-challenge-SurfsUp
assignment 10



### Climate Analysis and Data Exploration Using Python and SQLAlchemy

#### Precipitation Analysis

- Chose a start and end date for the trip, covering approximately 3-15 days.
- Utilized SQLAlchemy to establish a connection to the SQLite database.
- Employed SQLAlchemy's automap_base() to reflect tables into classes (Station and Measurement).

##### Query and Data Processing

- Designed a query to retrieve the last 12 months of precipitation data, focusing on date and precipitation values.
- Loaded query results into a Pandas DataFrame, setting the index to the date column, and sorted values by date.
- Plotted the results using the DataFrame plot method.
- Utilized Pandas to generate summary statistics for the precipitation data.

#### Station Analysis

- Crafted a query to determine the total number of stations.
- Developed a query to identify the most active stations, listing them in descending order of observation counts.
- Determined the station with the highest number of observations.

##### Temperature Observation Data (tobs)

- Designed a query to retrieve the last 12 months of tobs.
- Filtered data for the station with the highest number of observations.
- Plotted the results as a histogram.

#### Creating a Flask API

- Designed routes in Flask based on the aforementioned queries.
- Converted query results to a dictionary format, using date as the key and prcp as the value.
- Returned the JSON representation of the dictionary.
- Provided a JSON list of stations from the dataset.
- Queried for dates and temperature observations from a year from the last data point, returning a JSON list of Temperature Observations (tobs) for the previous year.
- Returned a JSON list of the minimum temperature (TMIN), average temperature (TAVG), and maximum temperature (TMAX) for a given start or start-end range. When given the start only, calculations included TMIN, TAVG, and TMAX for all dates greater than and equal to the start date. For a start-end range, calculations encompassed dates between the start and end date inclusive.

