## Cryptocurrency Market Data

### Introduction

**Cryptocurrencies** are getting relevance as rivals to traditional currency in certain parts of the world. The digital currencies are available to purchase in many different places, accessible to everyone. With retailers accepting various cryptocurrencies, it could be that money, as we know it, may go through a major change.

In addition, the **blockchain** technology on which many cryptocurrencies are based, with its revolutionary distributed digital backbone, has many other promising applications, such as **smart contracts**. Implementations of secure, decentralized systems can aid us in conquering organizational issues of trust and security that have plagued our society throughout the ages. Indeed, blockchain technology can disrupt industries core to economies, businesses and social structures, eliminating inefficiency and human error.

**Bitcoin**, created by the elusive Satoshi Nakamoto and released as open-source software in 2009, was the first cryptocurrency, and it is still the best known. It is the leader in capitalization and trading volume, followed by **Ethereum**, founded by Vitalik Buterin in 2015. The market cap of Bitcoin accounts for about 37% of the total cryptocurrency market cap.

The data for this project come in the well known OHLC (Open/High/Low/Close) format, complemented with some additional measures. Collected by Jesse Vent (`https://www.kaggle.com/jessevent/all-crypto-currencies`), they cover all cryptocurrencies (1,644), from April 28th, 20132, to June 6th, 2018.

### The data set

The actual data set has 13 fields and 785,024 records. The fields are:

* `slug`, a unique identifier of the coin, which corrects the duplication created by coins sharing the symbol.

* `symbol`, an identifier of the coin, with duplicates.

* `name`, the name of the coin.

* `date`, the date as yyyy-mm-dd.

* `ranknow`, the market capitalization rank by June 6th, 2018, from 1 to 1,644.

* `open`, the price (US dollar) of the stock at the beginning of the trading day. It can be different from the closing price of the previous trading day.

* `high`, the highest price (US dollar) of the stock on that trading day.

* `low`, the lowest price (US dollar) of the stock on that trading day.

* `close`, the price (US dollar) of the stock at closing time.

* `volume`, the amount of the coin that has been traded on that trading day.

* `market`, the market capitalization (US dollar), obtained by multiplying the circulating supply of coins by the current coin price. It provides a way to rank the relative size of a cryptocurrency.

* `close_ratio`, calculated as (close - low)/(high - low). In a few cases, for some minor coins, we find negative values in this field, because the closing price is lower than the lowest price, which does not make sense. This suggest that, for some coins, the data cannot be entirely trusted.

* `spread`, the difference between the high and low values for the day.

### Source

Kaggle.
