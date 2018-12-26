### Predicting Software Sales

### Introduction

*1C Company* (in Russian, *Фирма 1С*) is an independent Russian software developer and publisher, with headquarters in Moscow. It is a leader of the business software market, with a share of 33%, competing with worldwide leader *SAP*. With the creation of *1C International*, it started to compete also in other markets worldwide, including the United States, Europe, Middle East and East Asia. It is also known outside Russia as a video game developer, whose products are published for international platforms like the *Xbox*.

In the internal Russian market, *1C Company*'s leadership is clear in: (a) business software form Small Medium Sizes Enterprises, with its comprehensive suite *1C:Enterprise* (*1C:Предприятие*), and (b) localizing and publishing Russian-language versions of international software. For instance, more than half of popular Western video games are licensed and published by *1C Company*. 

The company has over 2000 employees. At present 8000 dealers from 600 cities cooperate with *1C Company*. About 7500 teams constitute the *1C:Franchising* partner network, which is a main channel of value-adding for *1C Company*'s products. Service-partners provide regular information and technological support for 1C  Company's software customers. 

The data for this project are daily historical sales from a collection of *1C Company* stores. Some questions that could be addressed with these data are:

* To predict total sales for every product and store in the next month.

The list of shops and products slightly changes every month. So, creating a robust model that can handle such situations is part of the challenge.

### The database

The database contains daily historical data from January 2013 to October 2015. It is formed by the following tables:

* The table `sales` contains daily sales data. The fields are:

    + `date`, as yyyy-mm-dd.

    + `date_block_num`, a consecutive month number, used for convenience. January 2013 is 0, February 2013 is 1,..., October 2015 is 33.

    + `shop_id`, unique identifier of a shop.

    + `item_id`, unique identifier of a product.

    + `item_price`, current price of an item.

    + `item_cnt_day`, number of products sold that day.

* The table `items` contains supplemental information about the items/products. The fields are:

    + `item_name`, name of that product.

    + `item_id`, unique identifier of a product.

    + `item_category_id`, unique identifier of a product category.

* The table `item_categories` contains supplemental information about the product categories. The fields are:

    + `item_category_name`, name of a product category.

    + `item_category_id`, nique identifier of a product category.

* The table `shops` contains supplemental information about the shops. The fields are:

    + `shop_name`, name of a shop.

    + `shop_id`, unique identifier of a shop.

### Source

Kaggle.
