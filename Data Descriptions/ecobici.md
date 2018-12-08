## EcoBici

### Introduction

EcoBici is the bicycle sharing system launched in February 2010 by the government of Mexico City. Initially launched with 85 docking stations and 1,200 distinctive red and white liveried bicycles, the network expanded many times, up to 480 stations with more than 6,800 bicycles. It has actually more than 170,000 members registered, and covers an area of 38 squared kilometers.

The system is run by a private company, Clear Channel Outdoor, but funded by the government with an initial investment of 75 million pesos (US$5,750,000). Users of the system are required to purchase an RFID card at a cost of 400 pesos (US$30) which will provide them with access to the bicycles for one year. For tourists, a 7-day card can be obtained for 300 pesos, a 3-day card for 180 pesos, and a single day card for 90 pesos. Use of a bicycle is free for the first 45 minutes; extra charges are applied for use beyond this time limit.

EcoBici station readers have a credit card slot at the bottom. You can register and pay (with any credit card) very simply by answering a few questions on the screen - no ID required, no passports, no forms to sign. Once you register on the screen, you are given a registration number and you put in your own PIN code. You can then get a bike at any station just using that registration number and PIN.

### The database

The database contains data on all the trips from February 2010 to December 2017, plus supplemental data on the stations. It is formed by the following tables:

* The table `trips` contains data about the trips. The fields are:

    + `Genero_Usuario`, the user's gender, with values 'F' and 'M'.

    + `Edad_Usuario`, the user's age in years.

    + `Bici`, unique ID for the bike.

    + `Ciclo_Estacion_Retiro`, ID of the station where the bike was picked.

    + `Fecha_Retiro`, the date the bike was picked, as yyyy-mm-dd.

    + `Hora_Retiro`, the time the bike was picked, as hh:mm:ss.

    + `Ciclo_Estacion_Arribo`, ID of the station where the bike was returned.

    + `Fecha_Arribo`, the date the bike was returned, as yyyy-mm-dd.

    + `Hora_Arribo`, the time the bike was returned, as hh:mm:ss.

* The table `location` contains the geographic coordinates of the stations. The fields are:

    + `Estacion`, unique ID for the station.

    + `Latitud`, latitude of the station.

    + `Longitud`, longitude of the station.

* The table `station_matrix` contains the distance and the duration of the shortest trip between every pair of stations. Note that, because of the traffic regulation, the distance and the duration are not the same both ways. The fields are:

    + `Ciclo_Estacion_Retiro`, ID of the station where the bike is picked.

    + `Ciclo_Estacion_Arribo`, ID of the station where the bike is returned.

    + `Distancia`, in meters.

    + `Duracion`, in seconds.

### Source

Ecobici.
