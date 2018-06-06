# IoT-UK-Nation-Database-APIs

The organisation end point can be accessed here: https://api.iotuk.org.uk/iotOrganisation.

The end point allows you to filter the IoT UK Nation database by the following fields:
 - Organisation postcode  (using `postcode=`)
 - Organisation town (using `town=`)
 - Organisation sic code (using `sic=`)
 - Organisation founding year (using `year=`)
 - Organisation NUTS region (using `nuts=`)
 
For example, to find all IoT businesses in the town of Leeds, you may call the URL:
https://api.iotuk.org.uk/iotOrganisation?town=Leeds
 
You may chain together these filters in any order and in any combination.  For example, to find all the IoT businesses in the town of Leeds founded in 2016, you may call the URL:
https://api.iotuk.org.uk/iotOrganisation?town=Leeds&year=2016

A full copy of the organisations in the IoT UK Nation database can be downloaded from Data Mill North by visiting the link: https://datamillnorth.org/dataset/iotuk-nation-database
 
 
