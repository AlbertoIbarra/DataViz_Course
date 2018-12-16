## Flight Delays in the NYC Area

### Introduction

Hadley Wickham, Chief Scientist at RStudio, has collected airline on-time data for all flights departing New York City (NYC) in 2013. The airports covered by the data are LaGuardia Airport (LGA), John F. Kennedy International Airport (JFK) and Newark International Airport (EWR).

The central theme of this project is to use these data to evaluate the occurrence of flight delay in the NYC aerea and the extent to which it can be predicted from the available data. Some sugested lines of analysis are:

* Examine the occurrence of missing data in these data sets. Can they be taken as 'missing at random'?

* Are there seasonal patterns in the departure delays?

* How feasible it is to predict the departure delay in a continuous scale? Or is it better to drop this approach and use a binary scale (it is frequently considered that a flight is delayed when the delay exceeds 15 minutes, but other cutoffs can be tried)?

* Does the destination make a difference with respect to departure delay? Or is better to regard it as a question on whether an airline is more or less reliable?

* Can bad weather be taken as a cause of departure delay in the NYC area?

* Is there a characteristic of the planes that makes delay more likely to happen?

### The database

The database includes five tables. In the last three tables, the data are not complete.

* The table `airlines` contains the look up airline names (16) from their carrier codes:

    + `carrier`, the two-letter abbreviation of the carrier name.

    + `name`, the full name of the carrier.

* The table `airports` contains metadata for all the airports (1,458) connected with the NYC area:

    + `faa`, the FAA airport code.

    + `name`, the usual name of the aiport.

    + `lon`, the longitude of the location of the airport.

    + `lat`, the latitude of the location of the airport.

    + `alt`, the altitude in feet of the airport.

    + `tz`, the timezone offset from GMT at the airport.

    + `dst`, the daylight savings time zone, taking values 'A' (Standard US DST, starting on the second Sunday of March and ending on the first Sunday of November), 'U' (unknown) and 'N' (non-existing).

    + `tzone`, the IANA time zone, as determined by GeoNames webservice.

* The table `flights` contains on-time data for all flights (336,776) that departed the NYC area in 2013:

        + `datetime`, the scheduled date and hour of the flight, as yyyy-mm-dd hh:mm:ss, in the local time zone.

    + `dep_time`, the actual departure time of the flight.
    
    + `arr_time`, the actual arrival time of the flight.

    + `sched_dep_time`, the scheduled departure time of the flight.
    
    + `sched_arr_time`, the scheduled arrival time of the flight.

    + `dep_delay`, the departure dela in minutes, with negative time representing early departure.
    
    + `arr_delay`, the arrival delay in minutes, with negative time representing early arrival.

    + `carrier`, the two-letter carrier abbreviation.

    + `tailnum`, the plane tail number.

    + `flight`, the flight number.

    + `origin`, the origin of the flight.

    + `dest`, the destination of the flight.

    + `air_time`, the amount of time spent in the air in minutes.

    + `distance`, the distance between the origin and destination airports in miles.

* The table `planes` contains plane metadata for all plane tailnumbers (3,322) found in the FAA aircraft registry:

    + `tailnum`, the plane tail number.

    + `year`, the year the plane was manufactured.

    + `type`, the type of plane.

    + `manufacturer`, the manufacturer of the plane. 
    
    + `model`, the model of the plane.

    + `engines`, the number of engines of the plane.
    
    + `seats`, the number of seats of the plane.

    + `speed`, the average cruising speed of the plane in mph.

    + `engine`, the type of engine.

* The table `weather` contains hourly meterological data for LGA, JFK and EWR:

    + `origin`, the weather station.

    + `datetime`, the date and hour of the recording, as yyyy-mm-dd hh:mm:ss.

    + `temp`, the temperature in Farenheit.

    + `dewp`, the dewpoint in Farenheit.

    + `humid`, the relative humidity in percentage scale.

    + `wind_dir., the wind direction in degrees.

    + `wind_speed`, the wind speed in mph.

    + `wind_gust`, the wind gust in mph.

    + `precip`, the precipitation in inches.

    + `pressure`, the sea level pressure in millibars.

    + `visib`, the visibility in miles.

### Sources

1. OpenFlights.org.

2. RITA, Bureau of Transportation Statistics.

3. FAA Aircraft Registry.

4. ASOS Network download from Iowa Environmental Mesonet.
