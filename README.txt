Using the Google Geocoding API with a Database and 
Visualizing data on Google Maps


In this project, I'm using the Google geocoding API
 to clean up some user-entered 
geographic locations of 
university names and then placing the data on a Google
Map.


You should install the SQLite browser to view and modify 
the databases 
from:

 http://sqlitebrowser.org/


The first problem to solve is that 
the Google geocoding
API is rate limited to 2500 requests per day.  
So we break the problem into two
 phases. 
 

In the first phase I take the input data in the file
(where.data) 
and read it one line at a time, and retreive the 
geocoded response and store it in a database (geodata.sqlite).

Before we use the geocoding API, we simply check to see if the data for that particular line of input is already retreived.

 
This process can be stopped at any time by removing the file
 geodata.sqlite


Run the geoload.py program.   This program will read the input 
lines in where.data
and for each line check to see if it is already 
in the database
and if we don't have the data for the location,

call the geocoding API to retrieve the data and store it in 
the database.


