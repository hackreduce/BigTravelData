# FlightStats Inc.

* Steven Stark, Product Manager for Flight Data, picture is attached
* David White, Chief Customer Officer, picture is attached

## Data Sets

* Flight History for calendar year 2011. One record for each scheduled flights worldwide.  Includes basic info such as airline, flight number, departure and arrival details, additional airport details, and flight time.  Also includes information regarding codeshare flights.  Total size is ~50 million records. This file contains 59 fields.
* Reference data for Airports.  Airport codes and names along with lat/long.
* Reference data for Airlines.  Airline codes, names and category.
* Aircraft Seating Reference.  File showing seating capacity for various airplanes.  May be carrier specific if provided.

Flight History, along with Airports and Airlines reference data, provides a complete picture of a year's worth of commercial scheduled flights world-wide. Data analysis possibilities include:

* how many flights are in the air at any given time?
* where are the busiest air spaces and airports?
* how many flights are delayed? 
* what are the patterns of delay?  location? dates? time of day? 
* what are the patterns around marketing arrangements in the industry? (i.e. codeshares)

Using data from other providers to track demand, it might be possible to spot geographic regions and/or dates when the capacity fell behind demand.

* `AVG_FARE file`: The average ticketed fare value by ticket date, by cabin class, and by O&D market for all markets ticketed on that date for full year 2011.

* `MARKET file`: Summary by O&D Market (not coupon level) passenger sales at the ticket level for all tickets issued in 2011.  Example:  For a ticket that is routed DCA-DFW-LAX-DCA, there will be two records in the MARKET file.  One will be for the outbound connection (DCA-DFW-LAX) and the other for the return (LAX-DCA).  This is a view the marketing and revenue management guys would use.

* `SEGMENT file`: Detail file of all flight coupons for tickets issued in calendar year 2011.


There are several keys to cross-reference and link these files, so if more detailed analysis is desired it can be done by linking the files together. 
 
Finally ... below are the estimated file sizes.  We have not finished pulling the final extracts, so these are estimates based on some days' sample data and may be slightly on the high end, but we estimate fairly close.  (Remember, you asked for big data!)


|File|Records|Filesize (GB)|
|----|-------|-------------|
|AVG_FARE|661,863,072|24.81|
|MARKET|1,251,268,720|118.93|
|SEGMENT|1,674,698,480|128.93|
