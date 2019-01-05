## EcoBici Trips

### Introduction

EcoBici is the bicycle sharing system launched in February 2010 by the government of Mexico City. It was initially launched with 85 docking stations and 1,200 distinctive red and white liveried bicycles. The network has been expanded many times, up to 480 stations with more than 6,800 bicycles. It has actually more than 170,000 members registered, covering an area of 38 squared kilometers.

The system is run by a private company, Clear Channel Outdoor, but funded by the government with an initial investment of 75 million pesos (US$5,750,000). Users of the system are required to purchase an RFID card at a cost of 400 pesos (US$30) which will provide them with access to the bicycles for one year. For tourists, a 7-day card can be obtained for 300 pesos, a 3-day card for 180 pesos, and a single day card for 90 pesos. The use of a bicycle is free for the first 45 minutes, extra charges are applied for use beyond this time limit. This system has been replicated, with some variations, in Buenos Aires.

EcoBici station readers have a credit card slot at the bottom. You can register and pay (with any credit card) very simply by answering a few questions on the screen - no ID required, no passports, no forms to sign. Once you register on the screen, you are given a registration number and you put in your own PIN code. You can then get a bike at any station just using that registration number and PIN.

### The database

The database contains data on all the trips from February 2010 to December 2017, plus supplemental data on the stations. It is formed by the following tables:

* The table `trips` contains data about the trips. The fields are:

    + `Genero`, the user's gender, taking values 'F' (female) and 'M' (male).

    + `Edad`, the user's age in years.

    + `Bici`, a unique ID for the bike.

    + `Estacion_Retiro`, a unique ID of the station where the bike was picked.

    + `Retiro`, the time the bike was picked, as yyyy-mm-dd hh:mm:ss.

    + `Estacion_Arribo`, ID of the station where the bike was returned.

    + `Arribo`, the time the bike was returned, as yyyy-mm-dd hh:mm:ss.

* The table `location` contains the geographic coordinates of the stations. The fields are:

    + `Estacion`, a unique ID for the station.

    + `Latitud`, latitude of the station.

    + `Longitud`, longitude of the station.

* The table `station_matrix` contains the distance and the duration of the shortest trip between every pair of stations. Note that, because of the traffic regulation, the distance and the duration are not the same both ways. The fields are:

    + `Estacion_Retiro`, described above.

    + `Estacion_Arribo`, described above.

    + `Distancia`, in meters.

    + `Duracion`, in seconds.

### Source

EcoBici Ciudad de México.
