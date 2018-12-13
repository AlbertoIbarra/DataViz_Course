## Melbourne Housing Market

### Introduction

At the turn of the year 2018, it is said that Melbourne is experiencing a housing bubble. Some experts say that it may burst soon. Maybe someone can find a trend or give a prediction? Which suburbs are the best to buy in? Which ones are value for money? Where's the expensive side of town? And more importantly, where should I buy a two-bedroom unit?

In search for a response, Tony Pino scraped publicly available results posted every week from `www.Domain.com.au`. Supplemental data (number of bedrooms, bathrooms and car spots, land size, building area and geographical coordinates) were scraped from orther sources.

###  The data set

The data set includes the selling price and a collection of attributes of 27,247 houses sold in Melbourne since January 2016. Only the houses for which is available have been included. This leaves out auctioned property.

The variables are:

* `Suburb`, the name of the suburb in which the house is located (345 suburbs).

* `Address`, the address of the house.

* `Rooms`, the number of rooms.

* `Type`, real estate type, taking values 'h' (house, cottage, villa, semi terraced), 'u' (unit, duplex) and 't' (townhouse).

* `Price`, price in Australian dollars.

* `Method`, method of selling, taking values 'S' (property sold), 'SP' (property sold prior), 'PI' (property passed in), 'VB' (vendor bid) and 'SA' (sold after auction).

* `SellerG`, real estate agent involved in the transaction (349 agents).

* `Date`, date the house has been sold, as yyyy-mm-dd.

* `Distance` from the Melbourne Central Business District, in kilometers.

* `Postcode`, post code (4-digit).

* `Bedroom`,  number of bedrooms.

* `Bathroom`, number of bathrooms.

* `Car`, number of car spots.

* `Landsize`, the lot size, in square meters.

* `BuildingArea`, the area occupied by the building, in square meters.

* `YearBuilt`, the year when the house was built.

* `CouncilArea`, governing council for the area.

* `Latitude`, in degrees.

* `Longitude`, in degrees.

* `RegionName`, general region (West, North West, North, North east, etc).

* `PropertyCount`, number of properties that exist in the suburb.

### Source

Kaggle.
