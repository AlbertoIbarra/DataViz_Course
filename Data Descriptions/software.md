## Predicting Software Sales

### Introduction

*1C Company* (in Russian, *Фирма 1С*) is an independent Russian software developer and publisher, with headquarters in Moscow. It is a leader of the business software market, with a share of 33%, competing with worldwide leader *SAP*. With the creation of *1C International*, it started to compete also in other markets worldwide, including the United States, Europe, Middle East and East Asia. It is also known outside Russia as a video game developer, whose products are published for international platforms like the *Xbox*.

In the internal Russian market, *1C Company*'s leadership is clear in business software for Small and Medium-Sized Enterprises, with its comprehensive suite *1C:Enterprise* (*1C:Предприятие*). It has also published Russian-language versions of international software. For instance, more than half of popular Western video games are licensed and published by *1C Company*. 

The company has over 2,000 employees. At present 8,000 dealers from 600 cities cooperate with *1C Company*. About 7,500 teams constitute the *1C:Franchising* partner network, which is a main channel of value-adding for *1C Company*'s products. Service-partners provide regular information and technological support for *1C Company*'s software customers. 

The data for this project are daily historical sales from a collection of *1C Company* stores. Some questions that could be addressed with these data are:

* Can we develop a model for predicting the total sales for every product and store in the next month? Since the list of shops and products changes slightly every month, creating a robust model that can handle such situations is part of the challenge.

* Which are the best-selling products? Is it worth to maintain such a wide range of products, given the distribution of the sales across products and categories and products.

* How is the distribution of sales across stores and weekdays?

* How are the returns distributed? Is there anything or anybody that can be taken as the culprit?

### The database

The database contains daily historical data from January 2013 to October 2015. It is formed by the following tables:

* The table `categories` (the original Russian version is the table `categories_ru`) is the list of the 84 product categories. It has two fields:

    + `category_name`, the name of the product category.

    + `category_id`, a unique identifier of the product category.

* The table `items` is a list of 22,170 items/products, with supplemental information. It has three fields:

    + `item_name`, name of the product.

    + `item_id`, a unique identifier of the product.

    + `category_id`, described above.

* The table `sales` contains daily sales data. It has 2,935,849 records. It has five fields:

    + `date`, the date as yyyy-mm-dd.

    + `shop_id`, a unique identifier of the shop.

    + `item_id`, described above.

    + `item_price`, the current price of the item.

    + `item_cnt_day`, the number of product units sold that day in that shop. A negative value indicates a return.

* The table `shops` (original version `shops_ru`) contains supplemental information about the 60 shops covered by the database. The fields are:

    + `shop_name`, the name of the shop.

    + `shop_id`, described above.

### Source

Kaggle.
