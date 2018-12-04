## A Sneak Peek into the Airbnb Activity in Boston

### Introduction

Airbnb is a peer-to-peer online marketplace and homestay network, which enables people to list or rent short-term lodging in residential properties, with the cost of such accommodation set by the property owner. The company receives percentage service fees from both guests and hosts in conjunction with every booking. It has over 2,000,000 listings in 34,000 cities and 191 countries.

Since 2008, guests and hosts have used Airbnb to travel in a more unique, personalized way. Instead of waking to overlooked "Do not disturb" signs, Airbnb travelers find themselves rising with the birds in a whimsical treehouse, having their morning coffee on the deck of a houseboat, or cooking a shared regional breakfast with their hosts.

Questions:

* Can you describe the vibe of each Barcelona neighborhood using listing descriptions?

* What are the busiest times of the year to visit Boston? By how much do prices spike?

* Is there a general upward trend of both new Airbnb listings and total Airbnb visitors to Boston?

Tasks:

* Modelling prices. Airbnb has an algorithm, called *Smart Pricing*, for suggesting prices to new listings.

* Predicting occupation.

* Sentiment analysis of the reviews.

### The database

The database is integrated by three tables:

* The table `calendar` contains detailed calendar data for listings in Boston. The fields are:

    + `listing_id`.

    + `date`.

    + `available`.

    + `price`.

* The table `listings` contains detailed listings in Barcelona. The fields are:

    + `id`

    + `listing_url`

    + `scrape_id`

    + `last_scraped`

    + `name`

    + `summary`

    + `space`

    + `description`.

    + `experiences_offered`.

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

* The table `reviews` contains detailed reviews for listings in Boston. The fields are:

    + `listing_id`

    + `id`

    + `date`

    + `reviewer_id`

    + `reviewer_name`

    + `comments`.

### Source

Inside Airbnb.
