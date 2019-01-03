PROOF OF CONCEPT, STAT TABLE: https://datastudio.google.com/u/0/reporting/1JXmm4VvWmhPLTDRJRDzrNl4E_wOxAYvd/page/CwNd


Table of Contents: 

'Data Cleaning.py' takes the raw data resulting from 'Game PDFs.py' and cleans it up. 
- breaks out the field goals from a list of made and missed into a table with aggregate made and missed depending on distance
- creates passer rating
- creates field goal long, FG%
- deletes u'\xa0' unicode character from webscrape data
- adds team names for each player
- aggregates all week-by-week csvs for season-long csvs

'Game Script.py' runs the season included in the 'dataOutputFresh.xlsx' by using Selenium to interface with www.whatifsports.com/ncaafb

'Game PDFs.py' saves all game pdfs to the filepath of your choice

'Remove html spaces.py' is redundant

'Scraping Guide Script.py' is an index for each stat in the box score's html via BeautifulSoup

'Standings.py' creates conference and divisional standings based on the week input 'userWk'

'Stat Scraper.py' grabs all the data from the box score PDFs that were saved to your account via 'Game Script.py'

'Strength of Schedule' is a formula that determines the difficulty of each team's schedule

'divisions.py' contains a dictionary for the divisions of each team, to be imported into Standings.py

'idDic.py' contains a dictionary for the ID numbers of each team, to be imported into Standings.py

'statPlay.py' allows you to tinker around with stat csvs in a python shell

'teamCon.py' contains a dictionary for the conferences of each team, to be imported into Standings.py

'tiebreakers' contains a string guide of each conference's tiebreaker scenarios


To-Do List: 
- Make season stat csvs for each grouping
- Standings tiebreakers
- use findTeam() to add team names to Season Stat csvs
- Championship games
- - Neutral: ACC, B10, B12, SEC, MAC
- - Home games: P12, MWC, SBC, CUSA, AAC

Wishlist:

- Look up punters, punt returners, and kick returners to attribute Punt, Punt Return, and Kick Return Yardage to someone
- Parse the play-by-play to be able to attribute each play to a player and stat
- Integrate Bill C's stat profiles?
- Grab color codes for teams, integrate into matplotlib?

Other Links:
Google Form Generator: https://script.google.com/d/1mF_FvFUMMU7eUBjKRslrjJSlZo4vGmIglcVDZCMnsTwIVWeSisQM08Hy/edit
