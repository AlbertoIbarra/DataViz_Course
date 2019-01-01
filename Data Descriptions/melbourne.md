## Melbourne Housing Market

### Introduction

At the turn of the year 2018, it is said that Melbourne is experiencing a housing bubble. Some experts say that it may burst soon. Maybe someone can find a trend or give a prediction? Which suburbs are the best to buy in? Which ones are value for money? Where's the expensive side of town? And more importantly, where should I buy a two-bedroom unit?

In search for a response, Tony Pino scraped publicly available results posted every week from `www.Domain.com.au`. Supplemental data (number of bedrooms, bathrooms and car spots, land size, building area and geographical coordinates) were scraped from other sources. Due to the limitations of these sources, missing values are frequent in the data collected. 

###  The data set

The data set includes the selling price and a collection of attributes of 27,247 houses sold in Melbourne since January 2016. Only the houses for which the price is available have been included. This leaves out auctioned property.

The variables are:

* `Suburb`, the name of the suburb in which the house is located (345 suburbs).

* `Address`, the address of the house.

* `Rooms`, the number of rooms.

* `Type`, real estate type, taking values 'h' (house, cottage, villa, semi terraced), 'u' (unit, duplex) and 't' (townhouse).

* `Price`, the price in Australian dollars.

* `Method`, the method of selling, taking values 'S' (property sold), 'SP' (property sold prior), 'PI' (property passed in), 'VB' (vendor bid) and 'SA' (sold after auction).

* `SellerG`, the real estate agent involved in the transaction (349 agents).

* `Date`, the date the house has been sold, as yyyy-mm-dd.

* `Distance`, the distance from the Melbourne Central Business District, in kilometers. A few values missing.

* `Postcode`, the post code (4-digit). A few values missing.

* `Bedroom`, the number of bedrooms. About one fourth of the values missing.

* `Bathroom`, the number of bathrooms. About one fourth of the values missing.

* `Car`, the number of car spots. About one fourth of the values missing.

* `Landsize`, the lot size, in square meters. About one third of the values missing.

* `BuildingArea`, the area occupied by the building, in square meters. More than one half of the values missing.

* `YearBuilt`, the year when the house was built. More than one half of the values missing.

* `CouncilArea`, governing council for the area. A few values missing.

* `Latitude`, in degrees. About one fourth of the values missing.

* `Longitude`, in degrees. About one fourth of the values missing.

* `RegionName`, general region (West, North West, North, North east, etc). A few values missing.

* `PropertyCount`, number of properties that exist in the suburb. A few values missing.

### Source

Kaggle.
