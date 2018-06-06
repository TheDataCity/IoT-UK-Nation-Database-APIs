# IoT-UK-Nation-Database-APIs

The organisation end point can be accessed here: https://api.iotuk.org.uk/iotOrganisation.

The end point does not require any user authorisation.

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
 
## Useful notes
### Postcode 
The postcode lookup works on a partial match.  You may search for "**LS**" and return any postcode that contains LS.  This would return all Leeds postcode area postcodes, as well as records which contain "**LS**" in the inward portion of the postcode.

Postcodes must be entered with the usual spacing.  For example:
https://api.iotuk.org.uk/iotOrganisation?postcode=LS19%207TU
will return a result but:
https://api.iotuk.org.uk/iotOrganisation?postcode=LS197TU 
will not.

### NUTS3 regions
The NUTS3 code is a convenient way of representing administrative areas in the UK.  A full list of UK NUTS3 codes can be found here:
https://en.wikipedia.org/wiki/NUTS_statistical_regions_of_the_United_Kingdom

To find all organisations located in the Leeds region, you may search using the NUTS3 code of "**UKE42**":
https://api.iotuk.org.uk/iotOrganisation?nuts=UKE42

You must use the full NUTS3 code for this lookup to work.  
 
