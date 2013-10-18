# Amadeus

* Tadhg Pearson - Senior Software Developer (note: may also participate to the event)

* Benjamin Bezine  - Innovation engineer (note: may also participate to the event)

* Landry Holi - Head of Corporate Innovation (still to be confirmed) - Please refer to Linkedin photos for Tadhg, myself and to the attached photo for Benjamin. Other remark: In addition, Amadeus plans to set up a hackers team that will participate to the Thack itself.

## Data sets

The data refers to airline search queries performed through online and offline travel agencies, this, during max 6 months in 2011 (still under final review by our IP legal team) as off September 2011, and throughout the world. Each air search query will be defined by  the date / time the query was made, an Origin & Destination (i.e. travelling from /to), the request date of the trip, potentially booking code requested (rem. booking code outlines to some extent the class of service, i.e. business vs. economy), and also eventually specific carrier requested. Note that the request could be made of multiple air segments (up to 6 segments max), e.g. Segment 1: from New York to Chicago and Segment 2: from Chicago to Los Angeles.

Today we have one folder per YEAR-MONTH of the requests containing one GZIPed CSV file per day (called <YYYY-MM-DD>.csv.gz). GZiped files for a given month do not exceed 10 GB (rather around 6 to 7 GB max)- so for 6 months, less than 60 GB max of Gziped data delivered.

Below further details of each data query:

```
Date (YYYY-MM-DD)
Time (hh:mm:ss)
Origin (= Seg1Departure)
Destination (calculated)
Round trip (1 if the last destination is the same as the origin, else 0)
NbSegments
Seg1Departure
Seg1Arrival    
Seg1Date (YYYY-MM-DD)
Seg1Carrier
Seg1BookingCode
Seg2Departure
Seg2Arrival
Seg2Date (YYYY-MM-DD)
Seg2Carrier
Seg2BookingCode
Seg3Departure
Seg3Arrival
Seg3Date (YYYY-MM-DD)
Seg3Carrier
Seg3BookingCode
Seg4Departure
Seg4Arrival
Seg4Date (YYYY-MM-DD)
Seg4Carrier
Seg4BookingCode
Seg5Departure
Seg5Arrival
Seg5Date (YYYY-MM-DD)
Seg5Carrier
Seg5BookingCode
Seg6Departure
Seg6Arrival
Seg6Date (YYYY-MM-DD)
Seg6Carrier
Seg6BookingCode
```

Below data query examples:

```
2013-07-07,00:00:01,FXP,DE,FRA,VLC,1,4,FRA,MAD,2013-10-15,IB,P,MAD,VLC,2013-10-15,IB,P,VLC,MAD,2013-10-22,IB,N,MAD,FRA,2013-10-22,IB,N

2013-07-07,00:00:01,FXX,CO,MDE,CLO,1,2,MDE,CLO,2013-08-20,AV,C,CLO,MDE,2013-08-27,AV,Y

2013-07-07,00:00:01,MPT,US,EWR,BCN,1,2,EWR,BCN,2013-09-29,SK,,BCN,EWR,2013-12-18,SK 
```

Several motivational and intellectual statements or questions that may inspire developers to participate ... e.g., an actual or rhetorical question that your data begs is a good format for this item!

Broadly speaking, this dataset enables:

* Airlines to optimise their routing capacity and routing expansion according to the demand coming from their indirect distribution network. 
* Travel agencies to optimise their merchandising or/and advertising processes according to the demand, thus optimise sales conversion. 
* Hoteliers / Tourist boards know from which origin people may come from when coming to their city/region - and so what potential action may be set.
        
More precisely, these general questions, can be supported partly through answers for the below underlying questions: 
        
* What are the most current and likely popular Origin & Destinations? 
* What are the most popular routes vs. these popular Origin & Destination? 
* From where travelers may be originating from for a given destination? 
* What are the initial preferences of travelers in terms of carrier or class of services? 
* When do people search and is there some kind of pattern between the season / time of search vs. origin & destinations? 
