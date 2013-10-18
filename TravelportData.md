BigTravelData
=============

Big Travel Data hackathon 


Company name: Travelport
Names: Abdoul Sylla, Sr Director Products and Ted Beatie, Partner Technical Specialist — both will be present for the event
Data Set: Shopping data
The data results from users requesting the best priced options for journeys using origin/destination and date information. Each response consists of a few priced options to hundreds of options (1 per row) with the data organized in comma-delimited files. The columns are as follow:
Currency
Total Price
Taxes
Validating Airline
Number of Stops
Duration of Flights
Origin
Destination
Departure Date/Time
Arrival Date/Time
Departure Terminal
Arrival Terminal
Marketing Carrier
Operating Carrier
Flight Number
Booking Class
Cabin
Number of Seats
Availability Source
Equipment Type
Farebasis Code
Passenger Type Code
Fare Type
Columns 5 though 23 repeat for a round-trip option (outbound followed by inbound). The format also handles multi-leg segments using a data separator.

The shopping data is a snapshot of the conditions in a market (origin/destination and dates)  — it's what shoppers see when they use an online travel agency. Several questions could be answered from this data. Example: What does it (usually) cost to fly from A to B? What's a good price and which airline got it? How do I get there? How do airlines compare? What are customers seeing? How do prices change over time and across days? Etc.
 
Below are 2 round-trip records  — New York (LGA – LaGuardia) to Chicago (ORD – O'Hare) on Feb 15th, returning on Feb 17th; the first one connects in Philadelphia (PHL) on both the outbound and the inbound the '|' character limits the legs; the second record represents a non-stop in both directions.
USD,340.60,61.53,US,0|0,00118,LGA|PHL,PHL|ORD,201302150854|201302151139,201302151000|201302151257,C|B,C|2,US|US,US|US,3173|1731,T |T ,E|E,001|001,C|C,E75|320,1M|1,TXA0NA2P,AD,SIP,0|0,00058,ORD|PHL,PHL|LGA,201302171155|201302171539,201302171450|201302171637,2|F,B|C,US|US,US|US,1167|4458,U |U ,E|E,001|001,C|C,734|DH8,1M|1,UXA0NA6P,AD,SIP
USD,834.80,78.52,DL,0,00145,LGA,ORD,201302151015,201302151200,A,2,DL,DL,5939,B,E,001,B,E75,1,BSHLGA,AD,ER,0,00307,ORD,LGA,201302171130,201302171437,2,A,DL,DL,5942,Q ,E,001,B,E75,1,Q0SHPLN,AD,SIP

From a size standpoint, we estimate the data to be around 2TB/day uncompressed — and about 200 GB (or less) when compressed — in individual CSV files, one for each response set.
