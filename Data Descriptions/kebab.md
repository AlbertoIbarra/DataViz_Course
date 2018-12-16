## The Kebab Factory Sales

### Introduction

The Kebab Factory is a family restaurant which operates in Harmah, Saudi Arabia, for the last years. The business is focused on dine-in and delivery. Given the current success, they opened a second branch on Thursday 27th, July 2017. A third branch followed on Saturday 13th, January 2018.

The data for this project are daily sales, which have been normalized for confidentiality reasons, in Saudi Arabia riyals (SAR) and in number of customers. There are some interesting questions that the managers of The Kebab Factory would like to examine:

* Did the total sales go up or down with the opening of new branches? How is the performance for the new branches?

* Which variables are more relevant?

* Is there a simple formula for predicting sales for each branch? (this will help the team reduce the waste).

* What is the lagging duration of the ads? How long does their effect last?

* The delivery fee through the HungerStation app (`www.hungerstation.com`) is 15 SAR. When it is offered for free to the customers, The Kebab Factory pays 7.5 SAR and the delivery company subsidizes 7.5 SAR. Is this a good idea? Is the increase in orders and sales worth the 7.5 SAR paid? Note the following: a) HungerStation charges The Kebab Factory a 17% fee on sales, b) sales through HungerStation make up 25% of sales on average, c) during the promotion days, free delivery sales through the app are 51% on average, and d) the cost of the goods delivered is 48%.

#### The data set

The data cover from 2017-02-14 to 2018-11-13. The variables are:

* `date` (string), as 'yyyy-mm-dd'.

* `weekday` (string), as Monday, Tuesday, etc. Note that the weekend in Saudi Arabia is Friday and Saturday.

* `branch1_sales` (numeric), daily sales in Branch 1, in SAR. The sales are zero the days the restaurant is not open.

* `branch2_sales` (numeric), daily sales in Branch 2, in SAR. The sales are zero the days the restaurant is not open. The first opening takes place on 2017-07-27.

* `branch3_sales` (numeric), daily sales in Branch 3, in SAR. The sales are zero the days the restaurant is not open. The first opening takes place on 2018-01-13.

* `branch1_count` (numeric), daily number of customers in Branch 1.

* `branch2_count` (numeric), daily number of customers in Branch 2.

* `branch3_count` (numeric), daily number of customers in Branch 3.

* `pay_day` (numeric), a dummy for the day in which the workers are paid their salaries.  

* `ramadan` (numeric), a dummy for the Ramadan days (these are fasting days, where Saudis do not eat during the day).

* `school_holiday` (numeric), a dummy for school holidays.

* `exam_day` (numeric), a dummy for exam days.

* `social_ads` (numeric), a dummy for days in which social media ads are posted.

* `hunger_station` (numeric), a dummy for days with promo for free delivery through the HungerStation app.

### Source

Abdulrahman	Alageel.
