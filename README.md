# Daily-air-quality-estimates-for-urban-centers-in-Africa
Implementation of an air quality model based on satellite data adapted from a Zindi winning solution

In this project, [Jonathan Whitaker](https://github.com/johnowhitaker) and Yasin Ayami present a method for predicting historical air quality (as measured by daily median PM2.5 concentration) for locations where no ground-based sensors are present, by using weather data and remote sensing data from sources like the Sentinel-5P satellite. Air quality data is obtained for 555 cities and supplemented by satellite and weather data. This is then used to build a model to predict the air quality for a given date and location. A [competition](https://zindi.africa/hackathons/urban-air-pollution-challenge) hosted by Zindi was used to crowd-source the creation of the model used, with the winning code forming the basis of our modelling approach. We used the trained model to create a new dataset of historical air quality predictions for
cities across Africa, available at ​ https://github.com/johnowhitaker/air_quality_prediction

You can view winner, [Nikhil Mishra's](https://github.com/nikhilmishradevelop), solution [here](https://github.com/nikhilmishradevelop/zindi-winning-solutions/tree/master/Urban%20Air%20Pollution%20Challenge%20by%20%23ZindiWeekendz).

## Implementing the model
View the model implentation on [South African Spatial Data Infrastructure (SASDI)](http://www.sasdi.net/metaview.aspx?uuid=deff781ad8d65537edb600e24e4ef7d3) 

Report: https://docs.google.com/document/d/1e1y-hwduVXcDYs8KxxoGSrK_LI5mCOpe-7WY_QkcdoI/edit?usp=sharing or as PDF ('AirQ Report.pdf')

Dashboard to view results: http://www.datasciencecastnet.com/airq/

### Accessing Predictions

The predictions can be found in the Data/results folder.
- za_cities_predictions contains the predictions for cities across South Africa
- pcs_predictions contains predictions for some additional population centers in South Africa
- af_cities_predicitons contains the predictions for major cities across Africa

### Replicating the project:

- Download the historical air quality measurements from https://aqicn.org/data-platform/covid19/ and store the files in Data/waqi_downloads 
- Run '1. WAQI Data Prep.ipynb' to merge the relevant data into a single csv file, which is stored in Data/intermediate/citypm25.csv
- Run '2. Fetch GEE Data.ipynb'. You can optionally downlaod the same input data for new locations as well, to make predicitons for later.
- Run '3. Modelling and Evaluation.ipynb'. This loads the training data, trains and evaluates a model and saves predictions.

If you'd rather just use the trained model, you can do this by following '4. Making Predictions for New Locations' which shows how to use the trained model to make predictions given a set of locations you're interested in. It goes through all the steps needed, from downloading the data from GEE to saving and displaying your predictions.
