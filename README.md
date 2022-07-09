This project uses the Google geocoding API to clean up some user-entered geographic locations of university names and then placing the data on a Google Map.

Install the SQLite browser to view and modify the databases from: http://sqlitebrowser.org/

Take input data in the file (where.data) and read it one line at a time, and retrieve the geocoded response and store it in a database (geodata.sqlite).
Before we use the geocoding API, we simply check to see if
we already have the data for that particular line of input.

geoload.py program reads the input lines in where.data and for each line check to see if it is already in the database and if no data for the location,
call the geocoding API to retrieve the data and store it in the database.

This project was completed using a subset of that data which isavailable at: http://py4e-data.dr-chuck.net/json so the api_key set to False in 
geoload.py.

You can try this with the API key by simply inputing it into the code

The geoload.py can be stopped at any time, and there is a counter to limit the number of calls to the geocoding API for each run.

Data in geodata.sqlite can be visualized using the (geodump.py) program.  This
program reads the database and writes tile file (where.js) with the location, latitude, and longitude in the form of executable JavaScript code.


open where.html in a browser to see the locations and hover over each map pin to find the location that the
geocoding API returned for the user-entered input. 
