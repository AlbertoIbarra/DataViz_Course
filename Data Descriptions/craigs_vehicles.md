## Vehicles for Sale from Craigslist

### Introduction

Craigslist is a classified advertisements website with sections devoted to jobs, housing, for sale, items wanted, services, community, gigs, résumés, and discussion forums. Craig Newmark began the service in 1995 as an email distribution list to friends, featuring local events in the San Francisco Bay Area. It became a web-based service in 1996 and expanded into other classified categories. It started expanding to other U.S. cities in 2000, and now covers 70 countries.

Nowadays, Craigslist provides the world's largest collection of used vehicles for sale. Nevertheless, it is very difficult to collect all of them in the same place. Austin Reese built a scraper for a school project and expanded upon it later to create this data set which includes every used vehicle entry from every North-American region on Craigslist.

### The data set

The data for this project were captured in October of 2018. They contain the most relevant information that Craigslist provides on car sales, including fields like price, condition, manufacturer, latitude/longitude, and 15 other categories. Blank entries indicate that the listing did not provide that information. Missing values are frequent in some fields.

The data set has 699,316 records. The fields are:

* `url`, link to listing.

* `site`, the ID of the Craigslist site in which that listing was posted. It comes as part of the URL. Example: in the URL `https://newyork.craigslist.org/mnh/ctd/d/2005-nissan-pathfinder-le-4x4/6719445914.html`, the site is 'newyork', which accounts for the New York City metropolitan area. Later in the same URL, 'mnh' refers to Manhattan. Some Craigslist sites cover large regions instead of individual metropolitan areas —- for example, the US state of Wyoming, or the region called California Gold Country.

* `price`, price of vehicle in US dollars.

* `year`, year of the vehicle.

* `make`, make of the vehicle. Example: 'hyundai'.

* `model`, model of the vehicle. Example: 'sonata'. 

* `condition`, condition of the vehicle, traking the values 'excellent', 'good', 'like new', 'fair', 'new' and 'salvage'.

* `cylinders`, the number of cylinders of the vehicle.

* `fuel`, fuel taken by the vehicle, taking the values 'gas', 'diesel', 'other', 'hybrid' and 'electric'.

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
