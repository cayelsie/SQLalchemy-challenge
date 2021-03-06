This analysis uses Python, SQLAlchemy, Flask and Pandas in Jupyter notebook to analyze and share climate data for an upcoming trip to Honolulu, Hawaii.

The initial analysis used jupyter notebook with SQLAlchemy to connect with a sqlite database containing information about temperature and precipitation from weather stations in the Honolulu area. A query pulled the last 12 months of precipitation data, which was then plotted using Pandas plot.

![](Images/ppt_levels.png)

Summary statistics were also calculated on the last 12 months of precipitation data. Additionally, the total number of weather stations was determined, as well as the most active weather station. The max, min and average temps recorded from the most active station. A query pulled the last 12 months of temperature data from the most active station, and this was plotted in a histogram format. This analysis can be found at climate_main.ipynb.

![](Images/temps_histo.png)

A Flask API was designed based on the intial analysis. All information returned is in JSON format. Available routes include: a complete list of precipitation information by date from each weather station, a complete list of weather stations, a complete list of dates and temperature observations for the last year of data from the most active weather station, and the minimum, maximum and average temperatures for a given date range determined by user input (either start date - last year of data OR start date - end date, determined by the user). This code is found in the app.py file.

![](Images/routes.PNG)

The first bonus analysis uses Pandas to determine if there is a meaningful difference between the temperature in June and December. The averages for June and December were calculated and then a t-test was run to determine significance. This analysis can be found at temp_analysis_bonus_1_main.

The second bonus analysis examined potential rainfall and temperatures across a trip date range of 8/1 - 8/7. The mix, max and avg temps for that range in a previous year were calculated for comparison and then plotted as a bar chart, using the avg temp as the bar height and the difference between the max and min temp as the error bar length.

![](Images/trip_avg.png)

The total rainfall at each weather station for a previous year was calculated for the trip date range in a previous year for comparison. Additionally, the daily normals (max, min and avg temps) were calculated for all data within the 8/1 - 8/7 range. This was plotted in an area plot as predicted daily normals for the trip. This analysis can be found at temp_analysis_bonus_2_main.

![](Images/daily_normals.png)
