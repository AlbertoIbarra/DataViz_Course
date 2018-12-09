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

#### The database

The data for this project come from the public release of an anonymized data base containing a sample of over 3 million grocery orders from more than 200,000 Instacart users. The data come in a relational set of files describing customers' orders over time. For each user, between 4 and 100 of their orders are provided, with the sequence of products purchased in each order. Also provided are the weekday and the hour of day the order was placed, and a relative measure of time between orders.

The database contains five tables. Most of the table and variable names should be self-explanatory.

* The table `aisles` has 2 fields and 134 records. The fields are `aisle_id` and `aisle`.

* The table `departments` has 2 fields and 18 recods. The fields are `department_id` and `department`.

* The table `order_products`, with 4 fields and 3,346,083 records, contains order contents for all cus- tomers. It specifies which products were purchased in each order. The fields are: `order_id`, `product_id`, `add_to_cart_order` and `reordered`. Here, `reordered = 1` indicates that the customer has a previous order that contains the product. Note that some orders have no reordered items.

* The table `orders` has 6 fields and 33,819,106 records. The fields are: order `id`, `user_id`, `order_number`, `order_dow` (day of week), `order_hour_of_day` and `days_since_prior_order`.

* The table `products` has 4 fields and 49,688 records. The fields are: `product_id`, `product_name`, `aisle_id` and `department_id`.

### Source

The Instacart Online Grocery Shopping Dataset 2017, accessed from `https://www.instacart.com/datasets/grocery-shopping-2017`.
