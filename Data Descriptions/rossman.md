## Rossmann Store Sales

### Introduction

Rossmann operates over 3,000 drug stores in seven European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.

To get ideas on how to create a robust prediction model, Rossmann has released data on daily sales for 1,115 stores located across Germany, including store, promotion, and competitor data. Reliable sales forecasts enable store managers to create effective staff schedules that increase productivity and motivation. Better prediction models would help store managers stay focused on what is most important to them: their customers and their teams.

### The database

The historical sales data cover for 1,115 Rossmann stores, from January 2013 to July 2015. Note that some stores in the database were temporarily closed for refurbishment.

* The table `sales` contains sales data. The fields are:

    + `Store`, a unique Id for each store.

    + `DayOfWeek`, day of the week (Monday = 1, Sunday = 7).

    + `Date`, as yyyy-mm-dd.

    + `Sales`, the turnover for any given day, in euros.

    + `Customers`, the number of customers on a given day.

    + `Open`, a dummy for a store being open.

    + `Promo`, a dummy for having a promotion on a given day.

    + `StateHoliday`, indicating state holidays. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. The values are: a = Public holiday, b = Easter holiday, c = Christmas and 0 = None.

    + `SchoolHoliday`, a dummy for a store being affected by the closure of public schools on a particular date.

* The table `store` contains supplemental information about the stores. The fields are:

    +  `StoreType`, differentiating four different store models. The values are: a, b, c and d.

    + `Assortment`, describing the assortment level. The values are: a = basic, b = extra and c = extended.

    + `CompetitionDistance`, the distance in meters to the nearest competitor store.

    + `CompetitionOpenSinceMonth`, the approximate month of the time the nearest competitor was opened.

    + `CompetitionOpenSinceYear`, the approximate year of the time the nearest competitor was opened.

    + `Promo2`, a dummy for a store having continuing and consecutive promotion.

    + `Promo2SinceWeek`, the calendar week when the store started participating in `Promo2`.

    + `Promo2SinceYear`, the year when the store started participating in `Promo2`.

    + `PromoInterval`, the consecutive intervals `Promo2` is started, naming the months the promotion is started anew. For instance,  'Feb/May/Aug/Nov' means each round starts in February, May, August, November of any given year for that store.

### Source

Kaggle.
