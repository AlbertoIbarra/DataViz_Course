## Santander Product Recommendation

### Introduction

Ready to make a down payment on your first house? Or looking to leverage the equity in the home you have? To support needs for a range of financial decisions, Santander Bank offers a lending hand to their customers through personalized **product recommendations**.

Under their current system, a small number of Santander’s customers receive many recommendations while many others rarely see any, resulting in an uneven customer experience. In a Kaggle competition, Santander challenged talented data scientists to develop a model for predicting which products their existing customers would use in the next month, based on their past behavior and that of similar customers. With a more effective recommendation system in place, Santander can better meet the individual needs of all customers and ensure their satisfaction.

Santander provided monthly data of customers behavior data, covering 17 months, to predict what new products customers will purchase. For this project, we use only one month of data (June 2016). We have performed a bit of preprocessing, picking only the customers: (a) living in Spain, (b) which are not employees, and (c) with age from 20 to 100 years old. We also dropped a few products with a very low number of subscribers.

### The data set

The actual data set covers 910,592 customers, which is an attractive sample size for a data scientist. It has 27 fields, containing some data on the customers themselves and information about the products subscribed, such as 'credit card', 'savings account', etc. The fields from 10 to 27 are dummies for having these products.

The fields are:

* `codpers`, a unique customer's ID.

* `genero`, the customer's gender, taking values 'F' (female) and 'M' (male).

* `edad`, the customer's age in years.

* `antiguedad`, the customer seniority in months.

* `tiprel_1mes`, the customer relation type on the current month, taking values 'A' (active) and 'I' (inactive).

* `index`, a foreigner index, taking value 'S' if the customer's birth country is different than the bank country, and 'N' otherwise.

* `cod_prov`,	the province code of the customer's address.

* `renta`, the gross annual income of the household in euros. About one fourth of the values are missing.

* `segmento`, a customer segmentation, taking values 'TOP', 'PARTICULARES' and 'UNIVERSITARIO'. A few values are missing.

* `cco_fin`, a dummy for having a current account.

* `cno_fin`, a dummy for having a payroll account.

* `ctma_fin`, a dummy for having a 'más particular' account.

* `ctop_fin`, a dummy for having a particular account.

* `deme_fin`, a dummy for having a medium-term deposit subscription.

* `dela_fin`, a dummy for having a long-term deposits subscription.

* `ecue_fin`, a dummy for having a e-account.

* `fond_fin`, a dummy for having a funds subscription.

* `hip_fin`, a dummy for having a mortgage.

* `plan_fin`, a dummy for having a pension plan.

* `pres_fin`, a dummy for having a loan.

* `reca_fin`, a dummy for paying the taxes through the bank.

* `tjcr_fin`, a dummy for having a credit card.

* `valo_fin`, a dummy for having a securities subscription.

* `viv_fin`, a dummy for having a home account.

* `nomina`, a dummy for receiving the payroll through the bank.

* `nom_pens`, a dummy for having 'nómina-pensión, a special combination.

* `recibo`, a dummy for having a direct debit arrangement for paying bills.

### Source

Kaggle.
