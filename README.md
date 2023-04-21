# Project-3
# Covid-19 Dashboard
# Datasets
* The COVID Tracking Project Data API
* GitHub
* World Health Organization 

# Architecture Diagram
![Architecture Diagram](https://user-images.githubusercontent.com/120051602/233499501-5728022e-87f8-41c8-874b-2f97e0fdd42b.png)

# ETL Process
* Extract: The covid-19 Tracking Project Data API and Github are our two major extaction points.

* Transform: Using Jupyter Notebook and pandas, we cleaned and reorganized the data according to our needs.

* Load: Looking at the unpredictable structure of our data from our sources, SQLite was our database of choice

# Flask
Our Flask app connects to the SQLite database and pulls in data, implements further transformation and hosts our API endpoints as follows:
* @app.route("/") The root endpoint directs the user to the index.html page which holds the visualization dashboard.
* @app.route("/dataCL/<state>") This endpoint pulls data from the SQLite database and returns a JSON format that is used by the dashboard.js to create an interactive chart which shows covid cases, deaths and hospitalization in US.
* @app.route("/dataJS/<state>") This endpoint pulls data from the SQLite database and returns a JSON format that is used by the app.js to create an interactive chart which shows vaccination progress in US.
* @app.route("/dataIG/<state>") This endpoint pulls data from the SQLite database and returns a JSON format that is used by the app.js to create an interactive chart which shows increased hospitalization, increased death, ICU information in US.
* @app.route("/dataIL/<state>") This endpoint pulls data from the SQLite database and returns a JSON format that is used by the logic.js to create an interactive choropleth chart which shows daily covid cases in US.

# Visualization
Our visualization dashboard consists of the following technologies:

* HTML/CSS
* Bootstrap
* D3.js
* Plotly.js
* Leaflet.js
* Chart.js