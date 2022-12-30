# Data_Engineering_Project_2

This is the second Data engineering project which needing to merge few datasets and then detecting the outliers if found and deal with them then create some feature engineering, after that creating research questions and apply on them some visualization to answer them.
---------------------------

The data set source -----> https://www.kaggle.com/datasets/usdot/flight-delays?resource=download

- airlines.csv
- airport.csv
- flights.csv

---------------------------
## Merging Datasets: -

So merging the dataset was by using the merge() function on some arguments had common values between the three datasets using left_on right_on features too for specifying the attributes of each dataset we merging on them.

Merging was conducted on the flight table because it is acting as the main dataset for being holding the most attributes and also for the name of the datasets package as the 2015 Flight Delays and Cancellations.

#### airlines dataset:

  From the airlines dataset the attribute AIRLINE was merged into the flights dataset matching the IATA_CODE in the airlines dataset and the AIRLINE attribute in flights dataset. This attribute is showing the name of the airline the flight is related.
  
  
#### airports dataset: -

These attributes were merged into the flights dataset:
  - AIRPORT  -  which is the name of the airport
  - CITY   -   city of the origin airport
  - STATE  -   state of the origin airport
  - COUNTRY -  country of the origin airport
  - LATITUDE  -   laltitude of the origin airport
  - LONGITUDE  -  longtitude of the origin airport

matching the common attribute from airports which is the IATA_CODE and the attribute ORIGIN_AIRPORT from the flights dataset.

------------------------------------------------------------------

## Feature Engineering: -

The features engineering that was added are: 
  - DATE   -   showing the data in date format instead of using year column, month column, and day column so gathering them all in one attribute
  - ORIGIN_AIRPORT_COORDINATES   -  this attribute is holding the latitude and longtitde of the origin airport
  - DELAY_TIME   -    this attributes is showing the total delay time occured in the flights 
  
  
-------------------------------------------------------------------
