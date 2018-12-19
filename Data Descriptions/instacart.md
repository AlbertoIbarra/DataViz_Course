## Instacart Market Basket Analysis

### Introduction

Whether you shop from meticulously planned grocery lists or let whimsy guide your grazing, our unique food rituals define who we are. Instacart (`www.instacart.com`), a grocery ordering and delivery app, aims to make it easy to fill your refrigerator and pantry with your personal favorites and staples when you need them. After selecting products through the Instacart app, personal shoppers review your order and do the in-store shopping and delivery for you.

Instacart’s data science team plays a big part in providing the shopping experience. Currently, they use transactional data to develop models that predict which products a user will buy again, try for the first time, or add to their cart next during a session.

Other questions of interest would be:

- What product is most likely to be ordered late at night?

- What aisles are more likely to be reordered from?

- Are fruits reordered more frequently than vegetables?

- What products tend to be purchased earlier in the day?

- What products are ordered in the evening?

### The database

The data for this project come from the public release of an anonymized data base containing a sample of over 3 million grocery orders from more than 200,000 Instacart users (The Instacart Online Grocery Shopping Dataset 2017). The data come in a relational set of files describing customers' orders over time. For each user, between 4 and 100 of their orders are provided, with the sequence of products purchased in each order. Also provided are the weekday and the hour of day the order was placed, and a relative measure of time between orders.

The database contains five tables. Note that Instacart has 21 departaments, every department has several aisles, and every aisle contains a collection of products. Example: the product called 'Chocolate Sandwich Cookies' is stored in an aisle called 'cookies cakes', which belongs to a department called 'snacks'.

* The table `aisles` has 2 fields and 134 records. The fields are 

    + `aisle_id`, a unique aisle ID.
    
    + `aisle`, the name of the aisle, such as 'cookies cakes'.

* The table `departments` has 2 fields and 21 recods. The fields are:

    + `department_id`, a unique department ID.
    
    + `department`, the name of the department, such as 'snacks'.

* The table `order_products`, with 4 fields and 3,346,083 records, contains order contents for all customers. It specifies which products were purchased in each order. The fields are: 

    + `order_id`, a unique order ID.
    
    + `product_id`, a unique product ID.
    
    + `add_to_cart_order`, the order in which that product entered in the shopping cart. 
    
    + `reordered`, a dummy for the customer having a previous order that contains the product. Note that some orders have no reordered items.

* The table `orders` has 6 fields and 33,819,106 records. The fields are:

    + order `id`, described above.
    
    + `user_id`, a unique customer ID.
    
    + `order_number`, ordinal for that order in the set of orders of that customer.
    
    + `order_dow`, day of the week in which the order was placed.
    
    + `order_hour_of_day`, hour of the day in which the order was placed.
    
    + `days_since_prior_order`, days elapsed between that order and the preceding order of the same customer.

* The table `products` has 4 fields and 49,688 records. The fields are: 

    + `product_id`, described above.
    
    + `product_name`, the name of the product.
    
    + `aisle_id`, described above.
    
    + `department_id`, described above.

### Source

Instacart.
