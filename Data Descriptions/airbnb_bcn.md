## A Sneak Peek into the Airbnb Activity in Barcelona

### Introduction

Airbnb is a peer-to-peer online marketplace and homestay network, which enables people to list or rent short-term lodging in residential properties, with the cost of such accommodation set by the property owner. The company receives percentage service fees from both guests and hosts in conjunction with every booking. It has over 2,000,000 listings in 34,000 cities and 191 countries.

Since 2008, guests and hosts have used Airbnb to travel in a more unique, personalized way. Instead of waking to overlooked 'Do not disturb' signs, Airbnb travelers find themselves rising with the birds in a whimsical treehouse, having their morning coffee on the deck of a houseboat, or cooking a shared regional breakfast with their hosts.

Airbnb has been releasing and updating data at the Inside Airbnb site (`www.insideairbnb.com`). The last update (November 2018) covers 84 areas, most of them in US and Europe. In this project, we use data from Barcelona, posted on April 8th, 2018. Some interesting questions that can addressed with these data are:

* Can you describe the vibe of each Barcelona neighborhood using listing descriptions?

* What are the busiest times of the year to visit Barcelona? By how much do prices spike?

* Is there a general upward trend of both new Airbnb listings and total Airbnb visitors to Barcelona?

* How many listings are in that particular neighbourhood and where are they?

* How many houses and apartments are being rented out frequently to tourists and not to long-term residents?

* How much are hosts making from renting to tourists (compare that to long-term rentals)?

* Which hosts are running a business with multiple listings and where they?

Or you can undertake more ambitious tasks, such as:

* Modeling prices. Airbnb has an algorithm, called *Smart Pricing*, for suggesting prices to new listings. Can you create a similar tool?

* Predicting occupation for future dates.

* Perform a sentiment analysis of the reviews.

* Perform a segmentation of the listings based on owners' descriptions.

### The database

The database is integrated by four tables:

* The table `calendar` contains detailed calendar data for listings in Barcelona. There are 4 fields and 6,443,345 records. The fields are:

    + `listing_id`, a unique listing's ID. 

    + `date`, the date, as yyyy-mm-dd.

    + `available`, a dummy for being available on that date.

    + `price`, the listing's price in US dollars. The price you see when you search Airbnb (with dates selected) is the total price divided by the number of nights you selected. The price shown is for the listing as a whole, not per person. Price per night can be lower if you book for several days.

* The table `listings` contains detailed listings in Barcelona. The language in the descriptions is typically English or Spanish (with exceptions). The text comes in UTF-8 encoding, so special characters may not be correctly shown in Windows machines (in Spanish words such as 'habitación') The fields are:

    + `listing_id`, described above.

    + `listing_url`, the listing's URL.

    + `name`, the listing's name. It is a minimal description,  intended to be appealing, such as 'Centric Bohemian next Ramblas&Macba'.

    + `summary`, a longer description.

    + `space`, another longer description, focusing on the space available, the comfort and the conveniences. Redundancy with the preceding field is typical.

    + `description`, the longest description, also subject to redundancy.

    + `neighborhood_overview`

    + `notes`

    + `transit`

    + `access`

    + `interaction`

    + `house_rules`

    + `thumbnail_url`

    + `medium_url`

    + `picture_url`

    + `xl_picture_url`

    + `host_id`

    + `host_url`

    + `host_name`

    + `host_since`

    + `host_location`

    + `host_about`

    + `host_response_time`

    + `host_response_rate`

    + `host_acceptance_rate`

    + `host_is_superhost`

    + `host_thumbnail_url`

    + `host_picture_url`

    + `host_neighbourhood`

    + `host_listings_count`

    + `host_total_listings_count`

    + `host_verifications`

    + `host_has_profile_pic`

    + `host_identity_verified`

    + `street`

    + `neighbourhood`

    + `neighbourhood_cleansed`

    + `neighbourhood_group_cleansed`

    + `city`

    + `state`

    + `zipcode`

    + `market`

    + `smart_location`

    + `country_code`

    + `country`

    + `latitude`

    + `longitude`

    + `is_location_exact`

    + `property_type`

    + `room_type`

    + `accommodates`

    + `bathrooms`

    + `bedrooms`

    + `beds`

    + `bed_type`

    + `amenities`

    + `square_feet`

    + `price`

    + `weekly_price`

    + `monthly_price`

    + `security_deposit`

    + `cleaning_fee`

    + `guests_included`

    + `extra_people`

    + `minimum_nights`

    + `maximum_nights`

    + `calendar_updated`

    + `has_availability`

    + `availability_30`

    + `availability_60`

    + `availability_90`

    + `availability_365`

    + `calendar_last_scraped`

    + `number_of_reviews`

    + `first_review`

    + `last_review`

    + `review_scores_rating`

    + `review_scores_accuracy`

    + `review_scores_cleanliness`

    + `review_scores_checkin`

    + `review_scores_communication`

    + `review_scores_location`

    + `review_scores_value`

    + `requires_license`

    + `license`

    + `jurisdiction_names`

    + `instant_bookable`

    + `cancellation_policy`

    + `require_guest_profile_picture`

    + `require_guest_phone_verification`

    + `calculated_host_listings_count`

    + `reviews_per_month`.

* The table `reviews` contains detailed reviews for listings in Barcelona. The fields are:

    + `listing_id`, described above.

    + `review_id`, a unique review's ID.

    + `date`, the review's date, as yyyy-mm-dd.

    + `reviewer_id`, a unique author's ID.

    + `reviewer_name`, the author's name.

    + `comments`, the text of the review..

### Source

Inside Airbnb.
