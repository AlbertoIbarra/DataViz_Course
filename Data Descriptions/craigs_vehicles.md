## Vehicles for Sale from Craigslist

### Introduction

Craigslist is a classified advertisements website with sections devoted to jobs, housing, for sale, items wanted, services, community, gigs, résumés and discussion forums. Craig Newmark began the service in 1995 as an email distribution list to friends, featuring local events in the San Francisco Bay Area. It became a web-based service in 1996 and expanded into other classified categories. It started expanding to other U.S. cities in 2000, and now covers 70 countries.

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

* `cylinders`, the number of cylinders of the vehicle, taking the values '3 cylinders', '4 cylinders', '5 cylinders', '8 cylinders', '10 cylinders', '12 cylinders' and 'other'.

* `fuel`, fuel taken by the vehicle, taking the values 'gas', 'diesel', 'other', 'hybrid' and 'electric'.

* `odometer`, miles the vehicle has been driven.

* `title_status`, title status of the vehicle, taking values 'clean' (this vehicle has all legal documents), 'lien' (this vehicle is subject to a lien), 'missing' (these documents are missing), 'parts only' (typically found on a bill of sale or transfer form, not on a title, but, if a parts only bill of sale is submitted for vehicle title processing, the title may be issued with a salvage brand or other cloud on title), 'rebuilt' (issued by an insurance company, body shop, collision center, or licensed rebuilder -- the vehicle insurance may have limits), 'salvage' (issued by an insurance company who pays a claim on the vehicle -- the vehicle incurs some type of loss event such as major damage, theft, or repair).

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
