### Santander Product Recommendation

#### Introduction

Ready to make a down payment on your first house? Or looking to leverage the equity in the home you have? To support needs for a range of financial decisions, Santander Bank offers a lending hand to their customers through personalized **product recommendations**.

Under their current system, a small number of Santander’s customers receive many recommendations while many others rarely see any, resulting in an uneven customer experience. In a Kaggle competition, Santander challenged talented data scientists to develop a model for predicting which products their existing customers would use in the next month, based on their past behavior and that of similar customers. With a more effective recommendation system in place, Santander can better meet the individual needs of all customers and ensure their satisfaction no matter where they are in life.

Santander provided 17 months years of customers behavior data to predict what new products customers will purchase. For this project, we use only one month of data (July 2016). We have performed a bit of preprocessing, picking only the customers: (a) living in Spain, (b) which are not employees, and (c) with age from 20 to 100 years old. We also dropped a few products with a very low number of subscribers.

After that, the data set covers 910,592 customers, which is an attractive sample size for a data scientist. It contains some data on the customers themselves, and information about the products subscribed, such as "credit card", "savings account", etc. Columns #10 - #27 are dummies for having these products.

The variables are:

* `sexo`, customer's sex.

* `age`, customer's age in years.

* `antiguedad`, customer seniority in months.

* `tiprel_1mes`, customer relation type at the beginning of the month: A (active), I (inactive), P (former customer), R (Potential).

* `indext`,	foreigner index: S if the customer's birth country is different than the bank country, N otherwise.

* `canal_entrada`, channel used by the customer to join (masked).

* `cod_prov`,	province code of the customer's address.

* `renta`, gross income of the household.

* `segmento`, customer segmentation: 01 - TOP, 02 - PARTICULARES, 03 - UNIVERSITARIO.

* `cco_fin`, current account.

* `cno_fin`, payroll account.

* `ctma_fin`, "más particular" account.

* `ctop_fin`, particular account.

* `deme_fin`, medium-term deposits.

* `dela_fin`, long-term deposits.

* `ecue_fin`, e-account.

* `fond_fin`, funds.

* `hip_fin`, mortgage.

* `plan_fin`, pension plan.

* `pres_fin`, loans.

* `reca_fin`, taxes.

* `tjcr_fin`, credit card.

* `valo_fin`, securities.

* `viv_fin`, home account.

* `nomina`, payroll.

* `nom_pens`, pensions.

* `recibo`, direct debit.

#### Source

`https://www.kaggle.com/c/santander-product-recommendation`
