# DOTA2-Match-Scraper

Python scripts to scrape DOTA 2 match data from the STEAM API to be used for Machine Learning.

The matches are chosen based on the "Very High Skilled" bracket where all players are present. Match length is set at a minimum of 20 minutes to filter out arranged matches (which seems to be pretty common).

The output is a CSV file where each row is the heroes picked in the match. First 113 columns are radiant heroes and the next 113 columns are dire heroes. A value of "1" means the hero was picked while "0" means the hero was not picked.

The next column records "Radiant" victory. If "Radiant" wins, the value is "1" and if "Dire" wins, the value is "0".

The subsequent 2 columns record the match start time and match duration. These values are recorded to ease eliminating repeated entries.