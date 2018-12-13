## Direct Marketing of Term Deposits

### Introduction

There are two main approaches for companies to promote products and/or services: through mass campaigns, targeting a general indiscriminate public, or through **direct marketing**, targeting a specific set of contacts. Nowadays, in a global competitive world, positive responses to mass campaigns are typically very low. Alternatively, direct marketing focuses on targets that assumably will be keener to that specific product/service, making these campaigns more attractive, because of their efficiency. But the increasingly vast number of marketing campaigns has reduced their effect on the general public. Furthermore, economical pressures and competition has led marketing managers to invest on direct campaigns with a strict and rigorous selection of contacts.

Due to the internal competition and the current financial crisis, there are huge pressures for European banks to increase their financial assets. One strategy is to offer attractive long-term deposit applications with good interest rates, in particular by using direct marketing campaigns. A Portuguese institution has been offering term deposits to its clients for the past two years, but in a way that the bank's board finds disorganized and inefficient. It looks as if too many contacts were made, for the subscriptions obtained.

The bank has been using its own contact-center to carry out direct marketing campaigns. The telephone was the dominant marketing channel, although sometimes with an auxiliary use of the Internet online banking channel (e.g. by showing information to a specific targeted client). Furthermore, each campaign was managed in an integrated fashion and the results for all channels were outputted together.

The manager in charge of organizing the next campaign is expected to optimize the effort. His objective is to find a **predictive model**, based on data of the preceding campaign, which can explain the success of a contact, i.e. if the client subscribes the deposit. Such model can increase the campaign's efficiency by identifying the main characteristics that affect success, helping in a better management of the available resources (e.g. human effort, phone calls and time) and the selection of a high quality and affordable set of potential customers. To be useful for the direct campaign, a predictive model should allow to reduce the number of calls in a relevant way without loosing a relevant number of subscribers.

### The data set

The data for this project come from the previous phone campaign of the bank, which involved a total of 45,211 contacts. During that campaign, an attractive long-term deposit application, with good interest rates, was offered. The contacts led to 5,289 subscriptions (11.7% success rate).

The data set combines demographic data with data about the interaction of the customer and the bank. The variables are:

* `age`, the client's age in years.

* `job`, the client's type of job, taking values 'admin', 'unknown', 'unemployed', 'management', 'housemaid', 'student', 'retired', 'self-employed, 'entrepreneur', 'technician' and 'services'.

* `marital`, the client's marital status, taking values 'married', 'divorced' and 'single'.

* `education`, the client's education level, taking values 'unknown', 'secondary', 'primary' and 'tertiary'.

* `default`, whether the client has credit in default, taking values 'yes' and 'no'.

* `balance`, the client's  average yearly balance in euros.

* `housing`, whether the client has a housing loan, taking values 'yes' and 'no'.

* `loan`, whether the client has a personal loan, taking values 'yes' and 'no'.

* `contact`, the usual communication channel, taking values 'unknown', 'telephone' and 'cellular'.

* `duration`, the duration of last contact before the campaign in seconds.

* `pdays`, the number of days passed by after the client was last contacted from a previous campaign. When the client has not been not previously contacted, it takes value -1.

* `previous`, the number of contacts performed before this campaign and for this client.

* `poutcome`, the outcome of the previous marketing campaign. The values are 'unknown', 'other', 'failure' and 'success'.

* `deposit`, whether the client has subscribed a term deposit, taking values 'yes' and 'no'.

### Source

S Moro, R Laureano & P Cortez (2011), Using data mining for bank direct marketing --- An application of the CRISP-DM methodology, *Proceedings of the European Simulation and Modelling Conference* (Guimarães, Portugal).
