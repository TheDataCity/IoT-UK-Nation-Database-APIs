# IoT-UK-Nation-Database-APIs

The organisation end point can be accessed here: https://api.iotuk.org.uk/iotOrganisation.

The end point does not require any user authorisation.

## Filters
You must use a filter with the end point.  If you do navigate to the base URL you will receive a warning message advising you to apply a filter.

The end point allows you to filter the IoT UK Nation database by the following fields:
 - Organisation postcode  (using `postcode=`)
 - Organisation town (using `town=`)
 - Organisation sic code (using `sic=`)
 - Organisation founding year (using `year=`)
 - Organisation NUTS region (using `nuts=`)
 - Organisation Westminster region (using `westminster=`)
 - Organisation Local Authority region (using `la=`)
 
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

### Westminster regions
The Westminster regions are defined in the National Statistics Postcode Lookup file.  To search for a westminster constituency, you will need to use the Westminster constituency code.  For example, to search for the Leeds Central constituency, you can use the code E14000777
https://api.iotuk.org.uk/iotOrganisation?westminster=E14000777

More details, and to find a list of Westminster region codes, please visit:
https://data.gov.uk/dataset/7ec10db7-c8f4-4a40-8d82-8921935b4865/national-statistics-postcode-lookup-uk

### Local Authority regions
The Local Authority regions are defined in the National Statistics Postcode Lookup file.  To search for a local authority area, you need need to use the Local Authority code.  For example, to search for Leeds, you can use the code E08000035
https://api.iotuk.org.uk/iotOrganisation?la=E08000035

More details, and to find a list of Local Authority region codes, please visit:
https://data.gov.uk/dataset/7ec10db7-c8f4-4a40-8d82-8921935b4865/national-statistics-postcode-lookup-uk

### Geographic lookups
The NUTS, Westminster and Local Authority geographies are provided as a convenience to the user in filtering the data on the assumption that the user would have access to the relevant codes to use.  The user may run a search for a postcode or a town and find the associated geographies returned in the data response from this endpoint.  Using this method may identify the relevant codes to search on for the user.



 
