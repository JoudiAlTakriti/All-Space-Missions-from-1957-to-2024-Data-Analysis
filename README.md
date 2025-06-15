# All Space Missions from 1957 to 2024 Data Analysis
## Introduction	
Analyzing space mission data from 1957 to 2024, this project narrates the compelling story of space exploration through quantitative insights.

## Data Details
Files Name: all_space_mission_launches.csv
Description: The data-sheet is collected from https://nextspaceflight.com/launches/past/?page=1 and includes all the space missions since the beginning of Space Race between the USA and the Soviet Union in 1957 till to-date (Feb 2024).
Dataset Details: This dataset contains 6711 records (Raws). Size: 901kB

## Data Table Scheme:
| Feature Name    | Data Type | Description                                                                        |
|-----------------|-----------|------------------------------------------------------------------------------------|
| Organisation    | string    | Company name                                                                       |
| Location        | string    | location of the launch                                                             |
| Datetime        | date      | Datum and time of the launch (dates between 1957 and 2024)                         |
| Details         | string    | rocket name                       |
| Rocket_Status   | string    | Status of the rocket (either Active or Retired)                                    |
| Price   | float    | Cost of the mission: in $ million                                   |
| Mission_Status  | string    | Status of the mission (either Success, Failure, Partial Failure, or Prelaunch Failure) |

Data Analysis
Data Wrangling
Created Country column: by separating the Location string details using =TEXTSPLIT(B2,”,”), Find and Replace, and Filters. So it becomes easier to use location in visualizations.
Changed some location names to a country name so it can be visualized in a map according to the location found on Google Maps: Barents Sea to Russia, China Coastal Waters to China, Gran Canaria to Spain, Pacific Missile Range Facility to USA, Pacific Ocean to Kiribati.
Created Day, Month, Year, Time columns by applying Split Text to Column. So analyzing date and time becomes easier.
Left Blank cells in Price Column empty, and converted the values to USD.
Data Table Scheme After Wrangling:


Analysis Methods:
 Data challenges:
Had to convert some locations to specific countries according to the location found on Google Maps or the internet.
4074 price values are missing (60.69% of price records are missing), leading to a large error in calculating the total and average money spent. Therefore, no analysis using prices will be done. 
Combined the mission launches that happened in Kazakhstan and Russia as the USSR in some charts between the years 1957 and 1991 to represent the Cold War between the USA and the USSR.
Combined the mission launches that happened in Kazakhstan and Russia, the USA and the Marshall Islands to be represented in one line chart.















Dashboard
The Dashboard ( Here ) introduces the space race story through data.













































