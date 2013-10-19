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
* 

## Flight History Data Description

```
name,example,Required?,description
flight_id,73528506,Y,The unique identifier for the flight
carrier_fs_code,DL,Y,The FlightStats code for the operating carrier
carrier_iata_code,DL,N,The IATA code for the operating carrier
carrier_icao_code,DAL,N,The ICAO code for the operating carrier
flight_number,1711,Y,The flight identification number and any additional characters
tail_number,N181UA,N,The tail number of the equipment for the flight.
is_codeshare,t,Y,t' if this a codeshare.  If so its information is duplicated except for the codeshareDesignator and marketing fields
codeshare_relationship,L,N,The codeshare relationship between this carrier and the operating carrier
marketing_carrier_fs_code,AF,N,The FlightStats code for the marketing carrier
marketing_carrier_iata_code,AF,N,The IATA code for the marketing carrier
marketing_carrier_icao_code,AFR,N,The ICAO code for the marketing carrier
marketing_flight_number,9056,N,The codeshare flight identification number and any additional characters
scheduled_equipment,M90,N,The equipment that was scheduled to be flown
actual_equipment,M90,N,The equipment that was actually flown
actual_equipment_icao_code,MD90,N,The ICAO code for the equipment that was actually flown
status,L,Y,"The current status of the flight: 'A' = Active, 'C' = Canceled, 'D' = Diverted, 'DN' = Data source needed, 'L' = Landed, 'NO' = Not Operational, 'R' = Redirected, 'S' = Scheduled, 'U' = Unknown"
departure airport,,,
departure_airport_fs_code,ATL,Y,The FlightStats code for the departure airport
departure_airport_iata_code,ATL,N,The IATA code for the departure airport
departure_airport_icao_code,KATL,N,The ICAO code for the departure airport
departure_terminal               ,N,N,The terminal from which the flight departed
departure_gate,B24,N,The gate from which the flight departed
published_departure,1/1/2013 16:45:00,N,The published departure time for the flight provided by the airline's published operating schedule
published_departure_utc,1/1/2013 11:45:00,N,The published departure time for the flight provided by the airline's published operating schedule
scheduled_gate_departure,1/1/2013 16:45:00,N,The scheduled gate departure for the flight. It may be the same as the published departure or it may have been updated
scheduled_gate_departure_utc,1/1/2013 11:45:00,N,The scheduled gate departure in UTC.
actual_gate_departure,1/1/2013 21:34:00,N,The actual gate departure time observed
actual_gate_departure_utc,1/1/2013 16:34:00,N,The actual gate departure in UTC
scheduled_runway_departure        ,1/1/2013 17:05:00,N,The scheduled runway departure time for the flight
scheduled_runway_departure_utc,1/1/2013 12:05:00,N,The scheduled runway departure in UTC.
actual_runway_departure           ,1/1/2013 21:44:00,N,The actual runway departure time observed
actual_runway_departure_utc,1/1/2013 16:44:00,N,The actual runway departure time in UTC.
arrival airport,,,
arrival_airport_fs_code              ,DFW,Y,The FlightStats code for the arrival airport
arrival_airport_iata_code              ,DFW,N,The IATA code for the arrival airport
arrival_airport_icao_code         ,KDFW,N,The ICAO code for the arrival airport
arrival_terminal                  ,C,N,The terminal into which the flight arrived
arrival_gate                      ,C7,N,The gate into which the flight arrived 
baggage_claim                     ,4,N,The baggage claim information for the arrival.
published_arrival                 ,1/1/2013 18:20:00,N,The published arrival time for the flight provided by the airline's published operating schedule.
published_arrival_utc                 ,1/1/2013 14:20:00,N,The published arrival time in UTC
scheduled_gate_arrival            ,1/1/2013 18:20:00,N,The scheduled gate arrival for the flight. It may be the same as the published arrival time or it may have been updated
scheduled_gate_arrival_utc,1/1/2013 14:20:00,N,The scheduled gate arrival in UTC
actual_gate_arrival               ,1/1/2013 22:54:00,N,The actual gate arrival time observed
actual_gate_arrival_utc,1/1/2013 18:54:00,N,The actual gate arrival in UTC
scheduled_runway_arrival          ,1/1/2013 18:31:00,N,The scheduled runway arrival time for the flight
scheduled_runway_arrival_utc,1/1/2013 14:31:00,N,The scheduled runway arrival in UTC
actual_runway_arrival             ,1/1/2013 22:48:00,N,The actual runway arrival time observed
actual_runway_arrival_utc,1/1/2013 18:48:00,N,The actual runway arrival in UTC
diverted_airport_fs_code,DAL,N,"The FlightStats code for the airport to which the flight was diverted, if any"
diverted_airport_iata_code,DAL,N,"The IATA code for the airport to which the flight was diverted, if any"
diverted_airport_icao_code,KDAL,N,"The ICAO code for the airport to which the flight was diverted, if any"
computed values,,,
scheduled_air_minutes,146,N,The calculated scheduled time in the air (runway to runway) in whole minutes
air_minutes,124,N,"The calculated time in the air (runway to runway) in whole minutes. This will be the actual air time if available, otherwise it will be the current best estimate."
scheduled_block_minutes,155,N,The calculated scheduled time between blocks (gate to gate) in whole minutes
block_minutes,140,N,"The calculated time between blocks (gate to gate) in whole minutes. This will be the actual block time if available, otherwise it will be the current best estimate."
departure_date_local,1/1/2013,Y,"The local date and time of the departure in ISO-8601 format (yyyy-MM-dd).  This value is likely the publishedDeparture or scheduledGateDeparture value, but could be some other operational value."
arrival_date_local,1/1/2013,Y,"The local date and time of the arrival in ISO-8601 format (yyyy-MM-dd).  This value is likely the publishedArrival or scheduledGateArrival value, but could be some other operational value."

```

## Airlines Description
```
name,example,Required?,description
airline_code,LCI,Y,FlightStats code for the airline
carrier_iata_code,LF,N,"IATA code for the airline, if any"
carrier_icao_code,LCI,N,"ICAO code for the airline, if any"
name,Lao Central Airlines Public Company,Y,"full name of the airline, which is not guaranteed to be current"
carrier_short_name,Leo Central Airlines,Y,shortened form of the name
carrier_category,I,Y,


Carrier Categories,
A,Scheduled Passenger Carrier
B,Non-Scheduled Passenger Carrier
C,Scheduled Cargo Carrier
D,Non-Scheduled Cargo Carrier
I,Scheduled Passenger/Cargo Carrier
J,Non-Scheduled Passenger/Cargo Carrier
```
## Airport Description

```
name,example,Required?,description
airport_code,RST,Y,FlightStats code for the airport
airport_iata_code,RST,N,IATA code for the airport
airport_icao_code,KRST,N,ICAO code for the airport
airport_faa_code,RST,N,FAA code for the airport
name,Rochester International Airport,Y,name of the airport
latitude,43.910793,N,
longitude,-92.489768,N,

```

## Aircraft Description

```
IATA Carrier Code,Two or three letter code assigned by IATA for this Carrier
ICOA Carrier Code,Two or three letter code assigned by ICAO for this Carrier
Carrier Name,Carrier Name
Service Type,"Type of service: J,S = passenger, F = cargo, Q = mixed configuration, U=surface passenger and V = surface cargo (provided when available)"
Filler,
Filler,
Filler,
Aircraft Type,The three letter code assigned by IATA for the specific aircraft type
First Seats,"The number of seats available in the first class cabin.  If provided by carrier, all seat numbers are specific to this carrier, otherwise the aircraft default or zero is used."
Filler,
Bus Seats,Business class seats.
Filler,
Premium Bus,Premiumn Business class seats.
Mobile Curtain,MC indicates the seats by class may vary
Econo Seats,Ecomomy class seats.
Filler,
Total Seats,Total seats
Filler,
Tonnage,Freight capacity shown in metric tons.
```

## Codeshares records

When one flight is marketed by other carriers, they FlightStats data will create separate records for each of the carriers.  
Each of these records will have the same 'flight_id' which is created by FlightStats.  Only one of these records 
will indicate 'is_codeshare=f'

Example below.  The first record is the carrier that actually operated this flight.  The other three are codeshares.
This sample pulled from Google spreadsheet.  The date format is different than the raw data file.

```
flight_id,carrier_fs_code,carrier_iata_code,carrier_icao_code,flight_number,tail_number,is_codeshare,codeshare_relationship,marketing_carrier_fs_code,marketing_carrier_iata_code,marketing_carrier_icao_code,marketing_flight_number,scheduled_equipment,actual_equipment,actual_equipment_icao_code,status,departure_airport_fs_code,departure_airport_iata_code,departure_airport_icao_code,departure_terminal,departure_gate,published_departure,published_departure_utc,scheduled_gate_departure,scheduled_gate_departure_utc,actual_gate_departure,actual_gate_departure_utc,scheduled_runway_departure,scheduled_runway_departure_utc,actual_runway_departure,actual_runway_departure_utc,arrival_airport_fs_code,arrival_airport_iata_code,arrival_airport_icao_code,arrival_terminal,arrival_gate,baggage_claim,published_arrival,published_arrival_utc,scheduled_gate_arrival,scheduled_gate_arrival_utc,actual_gate_arrival,actual_gate_arrival_utc,scheduled_runway_arrival,scheduled_runway_arrival_utc,actual_runway_arrival,actual_runway_arrival_utc,diverted_airport_fs_code,diverted_airport_iata_code,diverted_airport_icao_code,scheduled_air_minutes,air_minutes,scheduled_block_minutes,block_minutes,departure_date_local,departure_date_local_utc,arrival_date_local,arrival_date_local_utc
284636939,WS,WS,WJA,652,,f,,WS,WS,WJA,652,73H,,,L,YYC,YYC,CYYC,,D44,1/1/2013 12:20:00,1/1/2013 7:20:00,1/1/2013 12:20:00,1/1/2013 7:20:00,1/1/2013 12:18:00,1/1/2013 7:18:00,1/1/2013 12:30:00,1/1/2013 7:30:00,1/1/2013 12:32:00,1/1/2013 7:32:00,YYZ,YYZ,CYYZ,3,C39,,1/1/2013 6:04:00,1/1/2013 11:04:00,1/1/2013 6:04:00,1/1/2013 11:04:00,1/1/2013 6:06:00,1/1/2013 11:06:00,1/1/2013 5:57:00,1/1/2013 10:57:00,1/1/2013 5:51:00,1/1/2013 10:51:00,,,,207,199,224,228,1/1/2013,1/1/2013,1/1/2013,1/1/2013
284636939,WS,WS,WJA,652,,t,L,WS,DL,DAL,7118,73H,,,L,YYC,YYC,CYYC,,D44,1/1/2013 12:20:00,1/1/2013 7:20:00,1/1/2013 12:20:00,1/1/2013 7:20:00,1/1/2013 12:18:00,1/1/2013 7:18:00,1/1/2013 12:30:00,1/1/2013 7:30:00,1/1/2013 12:32:00,1/1/2013 7:32:00,YYZ,YYZ,CYYZ,3,C39,,1/1/2013 6:04:00,1/1/2013 11:04:00,1/1/2013 6:04:00,1/1/2013 11:04:00,1/1/2013 6:06:00,1/1/2013 11:06:00,1/1/2013 5:57:00,1/1/2013 10:57:00,1/1/2013 5:51:00,1/1/2013 10:51:00,,,,207,199,224,228,1/1/2013,1/1/2013,1/1/2013,1/1/2013
284636939,WS,WS,WJA,652,,t,L,WS,KE,KAL,6540,73H,,,L,YYC,YYC,CYYC,,D44,1/1/2013 12:20:00,1/1/2013 7:20:00,1/1/2013 12:20:00,1/1/2013 7:20:00,1/1/2013 12:18:00,1/1/2013 7:18:00,1/1/2013 12:30:00,1/1/2013 7:30:00,1/1/2013 12:32:00,1/1/2013 7:32:00,YYZ,YYZ,CYYZ,3,C39,,1/1/2013 6:04:00,1/1/2013 11:04:00,1/1/2013 6:04:00,1/1/2013 11:04:00,1/1/2013 6:06:00,1/1/2013 11:06:00,1/1/2013 5:57:00,1/1/2013 10:57:00,1/1/2013 5:51:00,1/1/2013 10:51:00,,,,207,199,224,228,1/1/2013,1/1/2013,1/1/2013,1/1/2013
284636939,WS,WS,WJA,652,,t,L,WS,AA,AAL,5194,73H,,,L,YYC,YYC,CYYC,,D44,1/1/2013 12:20:00,1/1/2013 7:20:00,1/1/2013 12:20:00,1/1/2013 7:20:00,1/1/2013 12:18:00,1/1/2013 7:18:00,1/1/2013 12:30:00,1/1/2013 7:30:00,1/1/2013 12:32:00,1/1/2013 7:32:00,YYZ,YYZ,CYYZ,3,C39,,1/1/2013 6:04:00,1/1/2013 11:04:00,1/1/2013 6:04:00,1/1/2013 11:04:00,1/1/2013 6:06:00,1/1/2013 11:06:00,1/1/2013 5:57:00,1/1/2013 10:57:00,1/1/2013 5:51:00,1/1/2013 10:51:00,,,,207,199,224,228,1/1/2013,1/1/2013,1/1/2013,1/1/2013

```

Sample from raw data file showing the datetime format, which is in 24 hour clock.
```
 flightstats_id | airline_iata_code | airline_icao_code | flight_number | scheduled_aircraft_type | is_codeshare | codeshare_designator | marketing_airline_iata_code | marketing_airline_icao_code | marketing_flight_number | origin_iata_code | origin_icao_code | origin_terminal | origin_gate | destination_iata_code | destination_icao_code | destination_terminal | destination_gate | baggage_claim | last_known_status | departure_date | published_departure | scheduled_gate_departure | actual_gate_departure | arrival_date |  published_arrival  | scheduled_gate_arrival | actual_gate_arrival 
      215086408 | Z3                |                   | 45            | DHC                     | f            |                      | Z3                          |                             | 45                      | KTN              | PAKT             |                 |             | MTM                   |                       |                      |                  |               | S                 | 2011-01-21     | 2011-01-22 00:00:00 | 2011-01-22 00:00:00      |                       | 2011-01-21   | 2011-01-22 00:12:00 | 2011-01-22 00:12:00    | 
      215086427 | Z3                |                   | 54            | DHC                     | f            |                      | Z3                          |                             | 54                      | HYL              |                  |                 |             | KTN                   | PAKT                  |                      |                  |               | S                 | 2011-01-21     | 2011-01-21 18:40:00 | 2011-01-21 18:40:00      |                       | 2011-01-21   | 2011-01-21 18:56:00 | 2011-01-21 18:56:00    | 

```


## Note about Scheduled Airtime
If Scheduled Airtime is provided in the data record it is sourced from flight plans provided by the carrier to the FAA.


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
