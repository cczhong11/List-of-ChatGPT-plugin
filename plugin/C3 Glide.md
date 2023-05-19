# C3 Glide

## Description for Model

C3 Glide retrieves live aviation data including METARs, TAFs, and NOTAMs for pilots. 

C3 Glide can retrieve METARs. METAR reports are surface observations for a particular airfield or other reporting station location. 

C3 Glide can retrieve TAFs. TAF reports are predictive atmospheric conditions for an area within five nautical miles of a particular airfield or other reporting station location. 

C3 Glide can retrieve NOTAMs. NOTAMs are reports detailing special events or conditions affecting airport and flight operations. These can include, but are not limited to runway closures, lack of radar services, rocket launches, hazard locations, airspace restrictions, construction updates, and unusual aircraft activity. 

The user provides one or more geographic locations, or reporting stations to retrieve the relevant live aviation data products. The geographic location(s), or reporting station(s) must be represented by ICAO airport codes (KJFK, EGLL, PHNL), IATA airport codes (MIA, LGA, HNL), and/or latitude and longitude coordinates (30.35,-81.013). Combined they can be represented as such: LEX;KATL;30.2,-82.1;KMCO. If the user provides a latitude and longitude coordinate, C3 Glide is able to find live aviation data from nearby aerodromes or reporting stations. 

The type(s) of live aviation data products best suited to the user’s requests are retrieved, including one or more of the following: METARs, TAFs, and/or NOTAMs. If NOTAMs are fetched, the NOTAM code must be specified as one of the following letters depending on the user query: 

'X' for All NOTAMs. 

'A' for Airspace, Control Zones, ADIZ, Air Traffic Procedures, SID, STARs, Air Traffic Services, Airspace Restrictions, VOLMET Services, Navigation Warnings, Terminal and Enroute Navigation Facilities, Navigation Beacons, Volcanic Activity, Unmanned Aircraft, and GNSS Services. 

'C' for Communications, SELCAL, Radar, and Surveillance. 

'F' for Facilities, Services, Firefighting Services, Fuel, Runways, Runway Surface Conditions, Aprons, Parking Areas, Taxiways, Lighting, Movement and Landing Areas. 

'I' for Instrument Approach Procedures, and Minimums. 

'O' for Obstacles, and Cranes. 

The user can supply a date and/or time for their request, which must be converted to UTC using the following format: 2021-12-07T16:37:00Z. The user date and/or time is captured as a period with a start, and end value. If a date and/or time is not supplied, the current UTC date and time is used.

