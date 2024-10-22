# Truck-fleet-Analysis---Big-Data-Project
This project aims to improve road safety by identifying hazardous truck drivers in California. We will analyze truck fleet data to uncover risk factors contributing to traffic incidents and develop strategies to reduce accidents and promote safer driving in the trucking industry.

# Datasets
Downloaded two datasets named geolocation.csv and trucks.csv from public govt websites (such as census.gov).

# Loaded the files to HDFS

# Created and derived further tables
From these two datasets, we derived :
* truck_mileage table from trucks table
* avg_mileage table from trucks_mileage
* drivermileage table from existing trucks_mileage
* events_count table from geolocation table
* riskfactor table from events_count and drivermileage table

# # Description of tables and datasets

** Geolocation table having truck, driver, events, geolocation details, speed of the truck, id's related to the events and the times vehicle had idling cases

** Trucks table with 4 year data from 2009 to 2013, containing miles and gas consumed

** truck_mileage table where we are deriving this table from trucks and stacking the values based on truckid, driverid, date, miles, gas and miles per gas (mpg)

** avg_mileage table derived from truck_mileage focusing on truckid and average mpg

** driver_mileage table derived from truck_mileage focusing on driver id and summation of miles covered by each of them

** events_count table by filtering the non-normal events from the 'geolocation' table and count occurrences for each driver

** riskfactor table -- output table -- Created by joining the result with the 'drivermileage' table and events_count to calculate total miles and risk factor

# Integrating HDFS with Tableau via JDBC drivers for Impala and Hive
Once the tables are created, connected them with Tableau using ODBC connector.

To improve the performance we used Impala for querying

# Conclusion
- refer to the .ppt file for more information on how to take measures and improve the performance


