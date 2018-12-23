## A Sneak Peek into the Airbnb Activity in Barcelona

### Introduction

Airbnb is a peer-to-peer online marketplace and homestay network, which enables people to list or rent short-term lodging in residential properties, with the cost of such accommodation set by the property owner. The company receives percentage service fees from both guests and hosts in conjunction with every booking. It has over 2,000,000 listings in 34,000 cities and 191 countries.

Since 2008, guests and hosts have used Airbnb to travel in a more unique, personalized way. Instead of waking to overlooked 'Do not disturb' signs, Airbnb travelers find themselves rising with the birds in a whimsical treehouse, having their morning coffee on the deck of a houseboat, or cooking a shared regional breakfast with their hosts.

Airbnb has been releasing and updating data at the Inside Airbnb site (`www.insideairbnb.com`). The last update (November 2018) covers 84 areas, most of them in US and Europe. In this project, we use data from Barcelona, captured on April 8th, 2018. Some interesting questions that can addressed with these data are:

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

    + `listing_id`, a unique listing's ID. An active listing is a property listed on Airbnb. Listings may include entire homes or apartments, private rooms or shared spaces. 

    + `date`, the date, as yyyy-mm-dd.

    + `available`, a dummy for being available on that date.

    + `price`, the listing's price in US dollars. The price you see when you search Airbnb (with dates selected) is the total price divided by the number of nights you selected. The price shown is for the listing as a whole, not per person. Price per night can be lower if you book for several days.

* The table `listings` contains detailed listings in Barcelona. The language in the descriptions is typically English or Spanish (with exceptions). The text comes in UTF-8 encoding, so special characters may not be correctly shown in Windows machines (in Spanish words such as 'habitación'). Some fields, in particular all the fields containing URL's, have been dropped. The remaining fields are:

    + `listing_id`, described above.

    + `name`, the listing's name. It is a minimal description (maximum 35 characters) of the place, intended to be appealing, such as 'Centric Bohemian next Ramblas&Macba'.

    + `summary`, a longer description (maximum 250 characters).

    + `space`, another longer description, focusing on the space available, the comfort and the conveniences. Redundancy with the preceding field is typical.

    + `description`, the longest description, also subject to redundancy.

    + `area_overview`, a description of the area.

    + `notes`, remarks posted by the host, such as 'no parties allowed', with many missing values.

    + `transit`, information about the public transportation in the area, with many missing values.

    + `access`, restrictions to the use of the space and rules about it, with many missing values.

    + `interaction`, details about the interaction with the host, with many missing values.

    + `house_rules`, rules such as 'forbidden to smoke', or respect the tranquility of the neighbors', with many missing values.
    
    + `host_id`, a unique host's ID.

    + `host_name`, the host's first name.

    + `host_since`, date the host started listing that property, as yyyy-mm-dd.

    + `host_location`, a town or country, not necessarily close to the property listed.

    + `host_about`, bio information about the host, with many missing values and lots of diversity.

    + `host_response_time`, taking the values 'a few days or more', 'N/A', 'within a day', 'within a few hours' and 'within an hour', with a few missing values. 

    + `host_response_rate`, percentage of new inquiries and reservation requests the host responded to (by either accepting/pre-approving or declining) within 24 hours in the past 30 days.

    + `host_acceptance_rate`, combined percentage of reservation requests the host accepted and booking inquiries he/she pre-approved or responded to with a Special Offer.

    + `host_is_superhost`, a dummy for being a Superhost. The minimum requirements for Superhosts are: (a) To have hosted at least 10 trips, (b) to have maintained a 90% response rate or higher, and (c) to have received a 5-star review at least 80% of the time been reviewed, as long as at least half of the guests who stayed with the host left a review. Once a host reaches Superhost status, a badge will automatically appear on their listing and profile to help you identify them.

    + `host_listings_count`, number of listings of that host in Barcelona.

    + `host_verifications`, a collection within square brackets, such as ['email', 'phone', 'reviews']. The verification process also helps to ensure that Airbnb and guests have someone who they can hold responsible in the event that a problem arises with a booking.    

    + `host_has_profile_pic`, dummy for the host including a picture in his/her profile, with a few missing values.

    + `host_identity_verified`, dummy for the host identified been verified, with a few missing values.
    
    + `neighborhood`, the neighborhood where the property listed is located. The neighborhoods, listed in the table `neighborhoods`, are taken from city or open source GIS files.

    + `zipcode`, the listing’s zipcode.

    + `latitude`, the listing’s latitude, in degrees.

    + `longitude`, the listing’s longitude, in degrees.

    + `is_location_exact`, a dummy for the exact listing’s location being shown on the map. At Airbnb, the host chooses between showing the general area of the listing or placing a small circular pin indicating the location with great accuracy.

    + `property_type`, the type of property listed. Typically 'Appartment', 'Bed & Breakfast' or 'House', but it can also be 'Boat', 'Loft', or others.

    + `room_type`, taking values 'Entire home/apt', 'Private room' and 'Shared room'.

    + `accommodates`, the maximum number of people that can comfortably fit in the listing.

    + `bathrooms`, the number of available bathrooms. With only a sink and a toilet, but no no shower or bathtub, the room counts as 0.5.

    + `bedrooms`, the number of available bedrooms.

    + `beds`, the number of available beds.

    + `bed_type`, taking values 'Airbed', 'Couch', 'Futon Pull-out Sofa' and 'Real Bed'.

    + `amenities`, a collection within curly braces, such as {TV,Internet,Wireless Internet,Air conditioning,Kitchen,Elevator in building,Buzzer/wireless intercom,Heating,Washer,Essentials,Shampoo}.

    + `square_feet`, square footage of the listing, with many missing values. 

    + `price`, described above.

    + `weekly_price`, the listing's weekly price in US dollars. Mostly missing.

    + `monthly_price`, the listing's weekly price in US dollars. Mostly missing.

    + `security_deposit` the security deposit in US dollars, with many missing values. Many hosts request a security deposit, but the money is not touched unless the host files a claim and Airbnb agrees to the charges.

    + `cleaning_fee`, the cleaning fee in US dollars, with many missing values. Hosts have the option of charging this in order to clean their space for a guest.

    + `guests_included`, maximum number of guests allowed.

    + `extra_people`, extra guest fee in US dollars.

    + `calendar_updated`, the last time the calendar of the listing has been updated, taking values such as 'never', 'today', 'yesterday', etc. Note that the data from the table `calendar` are valid only for the days the calendar is up to date.  

    + `availability_30`

    + `availability_60`

    + `availability_90`

    + `availability_365`

    + `number_of_reviews`, number of reviews of this listings that have been posted.
    
    + `first_review`, date of the first review, as yyyy-mm-dd.

    + `last_review`, date of the last review, as yyyy-mm-dd.

    + `review_scores_rating`, average reviewers' rating of overall experience (what was your guest’s overall experience?). Range 1-100, with many missing values.

    + `review_scores_accuracy`, average reviewers' rating of accuracy (how accurately did your listing page represent your space?). Range 1-10, with many missing values.

    + `review_scores_cleanliness`, average reviewers' rating of cleanliness (did your guests feel that your space was clean and tidy?). Range 1-10, with many missing values.

    + `review_scores_checkin`, average reviewers' rating of arrival (how smoothly did their check-in go?). Range 1-10, with many missing values.

    + `review_scores_communication`, average reviewers' rating of communication (how well did you communicate with your guest before and during their stay?). Range 1-10, with many missing values.

    + `review_scores_location`, average reviewers' rating of location (how did guests feel about your neighborhood?). Range 1-10, with many missing values.

    + `review_scores_value`, average reviewers' rating of value (did your guest feel your listing provided good value for the price?). Range 1-10, with many missing values.

    + `instant_bookable`, a dummy for Instant Book listings. Instant Book listings do not require approval from the host before they can be booked. 

    + `cancellation_policy`, cancellation policy, taking values 'flexible' (full refund within limited period), 'moderate' (full refund within limited period), 'strict' (full refund if cancellation is within 48 hours of booking), 'super_strict_30' ( 50% refund up until 30 days prior to check in), 'super_strict_60' (50% refund up until 60 days prior to check in) and 'long term' (first month not refundable, 30 day notice for cancellation).

    + `require_guest_profile_picture`, a dummy for requiring a guest profile picture.

    + `require_guest_phone_verification`, a dummy for requiring the guest phone verification.

    + `reviews_per_month`, average number of reviews per month, with many missing values.

* The table `reviews` contains detailed reviews for listings in Barcelona. The fields are:

    + `listing_id`, described above.

    + `review_id`, a unique review's ID.

    + `date`, the review's date, as yyyy-mm-dd.

    + `reviewer_id`, a unique author's ID.

    + `reviewer_name`, the author's name.

    + `comments`, the text of the review.

### Source

Inside Airbnb.
