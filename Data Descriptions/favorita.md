## Corporación Favorita Grocery Sales

### Introduction

Brick-and-mortar grocery stores are always in a delicate dance with purchasing and sales forecasting. Predict a little over, and grocers are stuck with overstocked, perishable goods. Guess a little under, and popular items quickly sell out, leaving money on the table and customers fuming.

The problem becomes more complex as retailers add new locations with unique needs, new products, ever transitioning seasonal tastes, and unpredictable product marketing. Corporación Favorita, a large Ecuadorian-based grocery retailer, knows this all too well. They operate hundreds of supermarkets, with over 200,000 different products on their shelves. They currently rely on subjective forecasting methods with very little data to back them up and very little automation to execute plans.

In search for help to build a model that more accurately forecasts product sales, Corporación Favorita has released sales data of 4,100 products in a sample of 48 stores located in Ecuador.  The data cover 4.5 years, from January 2013 to August 2017. The management at Corporación Favorita is excited to see how machine learning could better ensure they please customers by having just enough of the right products at the right time.

### The database

The data released include dates, store and item information, whether that item was being promoted, as well as the unit sales. Additional files include supplementary information that may be useful in building the models.

* The table `holiday_events` contains information on 350 events, national, regional and local. The fields are:

    + `date`, as yyyy-mm-dd.

    + `type`, the type of event, taking values 'Additional', 'Bridge', 'Event', 'Holiday', 'Transfer' and 'Work Day'.

    + `locale`, indicating the scope of the event. The values are `Local`, `National` and `Regional`.

    + `locale_name` of the locale related to the event. It can be a town, a region, or 'Ecuador', for national events.

    + `description`, the event commemorated.

    +  `transferred`, a Boolean field for the commemoration having been transferred to a different day (it only happens for some holidays).

* The table `items` contains information on the items sold. The fields are:

    + `item_nbr`, an ID for the product.

    + `family`, the product family. There are 33 families: 'BEAUTY', 'CLEANING', etc.

    + `class`, an ID for a class within a product family.

    + `perishable`, a dummy for the product being perishable.

* The table `oil` contains data on oil prices for the dates covered by the database. The fields are:

    + `date`, as yyyy-mm-dd.

    + `dcoilwtico`, the crude oil price (US dollars) for the West Texas Intermediate (WTI) quality in Cushing, Oklahoma.

* The table `stores` contains

    + `store_nbr`, an ID for the store.

    + `city`, the city where the store is located.

    + `state`, the province (Ecuador has 24 provinces).

    + `type`, the type of store, taking values 'A', 'B', 'C', 'D' and 'E'.

    + `cluster`, groups of stores.

* The table `unit_sales` contains data on unit sales by date, store and item. It does not include rows for items that had zero unit sales for a store/date combination. There is no information as to whether or not the item was in stock for the store on the date. The fields are:

    + `id`, an ID for the record.

    +	`date`, as yyyy-mm-dd.

    + `store_nbr`, an ID for the store.

    + `item_nbr`, an ID for the product.

    + `unit_sales`, the unit sales for that item on that date at that store. It can be integer (e.g., a bag of chips) or float (e.g., 1.5 kg of cheese). Negative values represent returns of that particular item.

    + `onpromotion`, whether that item was on promotion on that date at that store. Approximately 16% of the `onpromotion` values in this file are `NaN`.

* The table `transactions` contains data on the number of transactions per store and date. The fields are:

    + `date`, as yyyy-mm-dd.

    + `store_nbr`, an ID for the store.

    + `transactions` the number of transactions on that date at that store.

### Source

Kaggle.
