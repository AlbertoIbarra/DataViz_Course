## Vehicles for Sale from Craigslist

### Introduction

Craigslist is a classified advertisements website with sections devoted to jobs, housing, for sale, items wanted, services, community, gigs, résumés and discussion forums. Craig Newmark began the service in 1995 as an email distribution list to friends, featuring local events in the San Francisco Bay Area. It became a web-based service in 1996 and expanded into other classified categories. It started expanding to other U.S. cities in 2000, and now covers 70 countries.

Nowadays, Craigslist provides the world's largest collection of used vehicles for sale. Nevertheless, it is very difficult to collect all of them in the same place. Austin Reese built a scraper for a school project and expanded upon it later to create a data set which includes every used vehicle entry (category 'cars + trucks') from every North-American region on Craigslist.

### The data set

The data for this project were captured in October of 2018. They contain the most relevant information that Craigslist provides on car sales, including fields like price, condition, manufacturer, latitude/longitude, and 15 other categories. Blank entries indicate that the listing did not provide that information. Missing values are frequent in some fields.

The data set has 699,316 records. The fields are:

* `url`, the link to the listing.

* `site`, the ID of the Craigslist site in which that listing was posted. It comes as part of the URL. Example: in the URL `https://newyork.craigslist.org/mnh/ctd/d/2005-nissan-pathfinder-le-4x4/6719445914.html`, the site is 'newyork', which accounts for the New York City metropolitan area. Later in the same URL, 'mnh' refers to Manhattan. Some Craigslist sites cover large regions instead of individual metropolitan areas —- for example, the US state of Wyoming, or the region called California Gold Country.

* `price`, the price of vehicle in US dollars. The distribution has many unreliable values in both tails. For instance, there cars at one dollar, and cars at more than one billion dollars.

* `year`, the year of the vehicle. A few values missing, and some unreliable dates, such as year 302.

* `make`, the make of the vehicle. Example: 'hyundai'. A few values missing. 

* `model`, the model of the vehicle. Example: 'sonata'. A few values missing.

* `condition`, the condition of the vehicle, taking values 'excellent', 'fair', 'good', 'like new', 'new' and 'salvage'. About one third of the values missing.

* `cylinders`, the number of cylinders of the vehicle, taking values '3 cylinders', '4 cylinders', '5 cylinders', '8 cylinders', '10 cylinders', '12 cylinders' and 'other'. About one third of the values missing.

* `fuel`, the fuel taken by the vehicle, taking values 'diesel', 'electric', 'gas', 'hybrid' and 'other'. A few values missing.

* `odometer`, the number of miles the vehicle has been driven. About one third of the values missing. Same comment as for `price`, concerning unreliable data.

* `title_status`, the title status of the vehicle, taking values 'clean' (this vehicle has all legal documents), 'lien' (this vehicle is subject to a lien), 'missing' (these documents are missing), 'parts only' (typically found on a bill of sale or transfer form, not on a title, but, if a parts only bill of sale is submitted for vehicle title processing, the title may be issued with a salvage brand or other cloud on title), 'rebuilt' (issued by an insurance company, body shop, collision center, or licensed rebuilder -- the vehicle insurance may have limits), 'salvage' (issued by an insurance company who pays a claim on the vehicle -- the vehicle incurs some type of loss event such as major damage, theft, or repair). A few values missing.

* `transmission`, the transmission of the vehicle, taking values 'automatic', 'manual' and 'other'. A few values missing.

* `VIN`, the vehicle identification number. About two thirds of the values missing.

* `drive`, the drive of the vehicle, taking values '4wd', 'fwd' and 'rwd'. About one third of the values missing.

* `size`, the size of the vehicle, taking values 'compact', 'full-size','mid-size' and 'sub-compact'. About one third of the values missing.

* `type`, the vehicle type, taking values 'bus', 'convertible', 'coupe', 'hatchback', 'mini-van', 'offroad', 'other', 'pickup', 'sedan', 'SUV', 'truck', 'van' and 'wagon'. About one third of the values missing.
       
* `paint_color`, the color of the vehicle, taking the values 'black', 'blue', 'brown', 'custom', 'green', 'grey', 'orange', 'purple', 'red', 'silver', 'white' and 'yellow'. About two thirds of the values missing.

* `image_url`, a link to the image of the vehicle. A few values missing.

* `lat`, the latitude of the vehicle. According to Austin, not precise but very close. But there are unreliable values, such a car from Phoenix AR with a latitude corresponding to Antarctica. A few values missing.

* `long`, the latitude of the vehicle. Errors as in the latitude. A few values missing.

### Source

Kaggle.
