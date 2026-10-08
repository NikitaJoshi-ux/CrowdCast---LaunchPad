# CrowdCast---LaunchPad
#Current functionality: 
The current code collects live facility usage data from Purdue Recreation & Wellness and stores it for future crowd prediction.
The scraper uses Selenium to open Purdue’s live facility usage page and wait for the JavaScript-rendered occupancy data to load. It then uses BeautifulSoup to parse the rendered HTML and identify each facility.

For each facility, the code extracts:
- facility name
- current number of people
- maximum capacity
- percent full
- Purdue’s “last updated” time
- a timestamp for when CrowdCast collected the data


The collector is currently set to run every 10 minutes, so over time the CSV builds a historical dataset of crowd levels throughout the day.
The current pipeline is:
Purdue Facility Usage Page
        ↓
Selenium loads live data
        ↓
BeautifulSoup parses facility cards
        ↓
Pandas organizes the data
        ↓
CSV stores historical snapshots

**Right now, I only have DATA collection. Please feel free to make comments/improvements. 
