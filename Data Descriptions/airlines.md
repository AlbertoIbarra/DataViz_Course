## Airlines Reputation in Twitter

### Introduction

As companies focus on customer retention, they need data on customer satisfaction. The American Customer Satisfaction Index (ACSI), which started in 1994, is the only national cross-industry measure of customer satisfaction in the United States. The ACSI uses customer interviews as input to a multi-equation econometric model developed at the University of Michigan's Ross School of Business. The ACSI score is calculated as a weighted average of three survey questions which measure different facets of satisfaction with a product or service.

ACSI provides high quality data, allowing for comparison across industries. But it is published only once every year, so the effect of many actions taken by companies may fail to get reflected in the index. At the other extreme, even if measures derived from social network data have obvious biases and may be based on low quality text, they can be obtained at low cost and with high frequency. Twitter looks like a good candidate to provide this type of data. 

The airlines industry makes a good scenario to see the extent to which customer satisfaction measures derived from Twitter data can compete with those provided by the ACSI. Airlines rank low among the different industries covered by the ACSI. But there is no uniformity within the airlines industry. In 2018, among the nine airlines included in the index, Southwest Air, Alaska Air and JetBlue were ranked on top, while Fly Frontier and Spirit Airlines occupied the last places.

The data for this project have been extracted from the Twitter REST API, using the Twitter handles of the nine airlines mentioned above as search strings: '@AlaskaAir', '@Allegiant', '@AmericanAir','@Delta', '@FlyFrontier', '@JetBlue', '@SouthwestAir', '@SpiritAirlines' and '@united'. The database covers the whole month of December 2018.

### The data base

The data base available for this project contains nine tables, one for each company. The fields (names as provided by the Twitter API) are:

* `created_at`, coordinated universal ime (UTC) when the weet was created.

* `screen_name`, the 'screen_name' attribute of the user who posted the tweet.

* `account_created_at`, the 'created_at' attribute of the user who posted the tweet.

* `text`, the actual UTF-8 text of the tweet.

* `lang`, BCP 47 language identifier corresponding to the machine-detected language of the tweet's text, or 'und' if no language could be detected.

* `source`, app used to post the tweet.

* `is_retweet`, Boolean field for the tweet being a retweet.

* `retweet_count`, number of times the tweet has been retweeted.

* `followers_count`, the 'followers_count' attribute of the user who posted the tweet.

* `friends_count`, the 'friends_count' attribute of the user who posted the tweet.

* `favourites_count`, the 'favourites_count' attribute of the user who posted the tweet.

### Source

Twitter REST API.
