## The Kebab Factory Sales

### Introduction

 The Kekab Factory is a family business which has been operating at Harmah, Saudi Arabia, for the last years. The business is focused on food delivery. Given the current success, they opened a second branch on Thursday 27th, July 2017. A third branch followed on Saturday 13th, January 2018.

The data for this project are daily sales, in Saudi Arabia riyals (SAR), and in number of customers, of . There are some interesting questions that the managers of The Kebab Factory would like to examine:

* Did the total sales go up or down with the opening of new branches?

* Which variables are more important?

* Is there a simple formula for predicting sales for each branch? (this will help the team reduce the waste).

* What is the lagging duration of the ads? How long does their effect last?

* The delivery fee is 15 SAR. When it is offered for free to the customers, The Kebab Factory pays 7.5 SAR and the delivery company subsides 7.5 SAR. Is this a good idea? Is the increase in orders and sales worth the 7.5 SAR paid?

####  The data set

The data cover from 2017-02-14 to 2018-11-13. The variables are:

* `date` (string), as "yyyy-mm-dd".

* `weekday` (string): Monday, Tuesday, etc.

* `branch1_sales` (numeric), daily sales in Branch 1, in USD. Sales are zero when the restaurant is not open.

* `branch2_sales` (numeric), daily sales in Branch 2, in USD. Sales are zero when the restaurant is not open. First opening on 2017-07-27.

* `branch3_sales` (numeric), daily sales in Branch 3, in USD. Sales are zero when the restaurant is not open. First opening on 2018-01-13.

* `branch1_count` (numeric), daily number of customers in Branch 1.

* `branch2_count` (numeric), daily number of customers in Branch 2.

* `branch3_count` (numeric), daily number of customers in Branch 3.

* `pay_day` (numeric), a dummy for the day in which the workers are paid their salaries.  

* `ramdhan` (numeric), a dummy for the Ramdhan days (these are fasting days).

* `school_holiday` (numeric), a dummy for school holidays.

* `exam_day` (numeric), a dummy for exam days.

* `social_ads` (numeric), a dummy for days in which social media ads are posted.

* `hunger_station` (numeric), a dummy for days with promo for free delivery.

### Source

Abdulrahman	Alageel.
