# All Space Missions from 1957 to 2024 Data Analysis Report
## Introduction	
Analyzing space mission data from 1957 to 2024, this project narrates the compelling story of space exploration through quantitative insights.

## Data Details
Files Name: all_space_mission_launches.csv

Description: The data-sheet is collected from [here](https://nextspaceflight.com/launches/past/?page=1) and includes all the space missions since the beginning of Space Race between the USA and the Soviet Union in 1957 till to-date (Feb 2024).

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

## Data Analysis
### Data Wrangling
1. Created Country column: by separating the Location string details using =TEXTSPLIT(B2,”,”), Find and Replace, and Filters. So it becomes easier to use location in visualizations.
2. Changed some location names to a country name so it can be visualized in a map according to the location found on Google Maps: Barents Sea to Russia, China Coastal Waters to China, Gran Canaria to Spain, Pacific Missile Range Facility to USA, Pacific Ocean to Kiribati.
3. Created Day, Month, Year, Time columns by applying Split Text to Column. So analyzing date and time becomes easier.
4. Left Blank cells in Price Column empty, and converted the values to USD.

### Data Table Scheme After Wrangling:

| Column Name         | Type    | Description                                                                        |
|---------------------|---------|------------------------------------------------------------------------------------|
| Company             | string  | Company name                                                                       |
| Location (Country)  | string  | Country or location of the launch                                                  |
| Day                 | string  | Day of launch (Sat through Fri)                                                    |
| Month               | string  | Month of launch (Jan through Dec)                                                  |
| Year                | integer | Year of launch (1957 through 2024)                                                 |
| Time                | time    | Time of launch (00:00 through 23:59)                                               |
| Details             | string  | Rocket name                                                                        |
| Rocket_Status       | string  | Status of the rocket (either Active or Retired)                                    |
| Price (USD Million) | float   | Cost of the mission: in $ million                                                  |
| Mission_Status      | string  | Status of the mission (either Success, Failure, Partial Failure, or Prelaunch Failure) |


### Data challenges:
1. Had to convert some locations to specific countries according to the location found on Google Maps or the internet.
2. 4074 price values are missing (60.69% of price records are missing), leading to a large error in calculating the total and average money spent. Therefore, no analysis using prices will be done. 
3. Combined the mission launches that happened in Kazakhstan and Russia as the USSR in some charts between the years 1957 and 1991 to represent the Cold War between the USA and the USSR.
4. Combined the mission launches that happened in Kazakhstan and Russia, the USA and the Marshall Islands to be represented in one line chart.

## Dashboard
The Tableau story [Here](https://public.tableau.com/views/Book1_17485154805190/TheSpaceRaceStory?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) introduces the space race story through data.

<img width="1007" alt="Screen Shot 2025-06-13 at 7 38 51 PM" src="https://github.com/user-attachments/assets/c652143c-85b6-495d-94bc-aa73446e96e7" /><img width="981" alt="Screen Shot 2025-06-13 at 7 39 26 PM" src="https://github.com/user-attachments/assets/b2e5a438-3a0e-4294-adbd-90154c23509d" />
<img width="1005" alt="Screen Shot 2025-06-13 at 7 39 08 PM" src="https://github.com/user-attachments/assets/ccdfa05b-f435-49ca-a3c6-d548e02eec08" />









































