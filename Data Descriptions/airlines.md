## Airlines Reputation in Twitter

### Introduction

As companies focus on customer retention, they need data on customer satisfaction. The American Customer Satisfaction Index (ACSI), which started in 1994, is the only national cross-industry measure of customer satisfaction in the United States.

The ACSI uses customer interviews as input to a multi-equation econometric model developed at the University of Michigan's Ross School of Business. The ACSI score is calculated as a weighted average of three survey questions that measure different facets of satisfaction with a product or service.

Airlines rank very low among the different industries in the ACSI. But there is no uniformity within the airline industry. In 2018, among the nine airlines included in the index, Southwest, Alaska and JetBlue were ranked on top, while Frontier and Spirit occupied the last places.

Of course, ACSI provides high quality data, and allow for comparison across industries, but it is published yearly, so the effect of many actions taken by companies may fail to get reflected in the index. At the other extreme, even if measures derived from social network data have obvious biases and may be based on low quality text, they can be obtained at low cost and with high frequency.

Twitter looks like a good candidate to provide this type of data. The data for this project have been extracted from the Twitter REST API, using the Twitter names of the nine airlines mentioned above as search strings: '@AlaskaAir', '@Allegiant', '@AmericanAir','@Delta', '@FlyFrontier', '@JetBlue', '@SouthwestAir', '@SpiritAirlines' and '@united'. They cover the whole month December 2018.

### The data base

The data base available for this project contains nine tables, one for each company. The fields are:

* `created_at`, UTC time when this weet was created.

* `screen_name`, the 'screen_name' attribute of the user who posted the tweet.

* `account_created_at`, the 'created_at' attribute of the user who posted the tweet.

* `text`, the actual UTF-8 text of the status update.

* `lang`, BCP 47 language identifier corresponding to the machine-detected language of the tweet text, or 'und' if no language could be detected.

* `source`, utility used to post the tweet.

* `is_retweet`, Boolean field for the tweet being a retweet.

* `retweet_count`, number of times the tweet has been retweeted.

* `followers_count`, the 'followers_count' attribute of the user who posted the tweet.

* `friends_count`, the 'friends_count' attribute of the user who posted the tweet.

* `favourites_count`, the 'favourites_count' attribute of the user who posted the tweet.

### Source

Twitter REST API.
