## Vehicles for Sale from Craigslist

### Introduction

Craigslist is a classified advertisements website with sections devoted to jobs, housing, for sale, items wanted, services, community, gigs, résumés, and discussion forums. Craig Newmark began the service in 1995 as an email distribution list to friends, featuring local events in the San Francisco Bay Area. It became a web-based service in 1996 and expanded into other classified categories. It started expanding to other U.S. cities in 2000, and now covers 70 countries.

Nowadays, Craigslist provcides the world's largest collection of used vehicles for sale. Nevertheless, it is very difficult to collect all of them in the same place. Austin Reese built a scraper for a school project and expanded upon it later to create this data set which includes every used vehicle entry from every North-American region on Craigslist.

### The data set

The data for this project were taken in October of 2018. They contain most all relevant information that Craigslist provides on car sales including columns like price, condition, manufacturer, latitude/longitude, and 15 other categories. Blank entries indicate that the listing did not provide said information.

The data set has 1.72 million of rows and 20 columns. The columns are:

* `url` (string), link to listing.

* `city` (string), Craigslist region in which that listing was posted.

* `price` (numeric), price of vehicle.

* `year` (numeric), year of the vehicle.

* `manufacturer` (string), make of the vehicle.

* `make` (string), make of the vehicle.

* `condition` (string), condition of the vehicle.

* `cylinders` (string), number of cylinders of the vehicle.

* `fuel` (string), fuel taken by the vehicle.

* `odometer` (numeric), miles the vehicle has been driven.

* `title_status` (string), title status of vehicle (e.g. clean - this vehicle has all legal documents. missing - these documents are missing).

* `transmission` (string), transmission of the vehicle.

* `VIN` (string), vehicle identification number.

* `drive` (string), drive of the vehicle.

* `size` (string), size of the vehicle.

* `type` (string), vehicle type.

* `paint_color` (string), color of the vehicle.

* `image_url` (string), link to the image of the vehicle.

* `lat` (numeric), latitude of the vehicle, not precise but very close.

* `long` (numeric), latitude of the vehicle, not precise but very close.

### Source

Kaggle.
