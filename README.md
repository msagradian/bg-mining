# bg-mining
<<<<<<< HEAD
Exploring patterns and anomalies in backgammon
Soccerway
=========

Soccerway.com scrapping with R. May be some data exploration will be added.

### R files in "code" folder:
* ***soccerwayTeam.R*** - contains a function *soccerwayTeam(url)*. Takes url for the team squad info (for example, 
 see *data/URLpattern.txt* file) and reads the table.
* ***teamIDs.R*** - contains *teamIDs(url)*. Takes the page such as this: 
"http://int.soccerway.com/national/england/premier-league/20132014/regular-season/r21322/" and reads team IDs.
* ***loadSquadInfos.R*** - contains a function *loadSquadInfos(url,seasID,folder)*, which loads squad info for all the teams in the specified league at specified season and loads it to the choosen folder. For the details about url and seasID parameters, see *data/League URLs.txt*. 
Some details: by default, the *folder* parameter is set to NULL. With this value, function does not creates           any files. The *returnData* parameter determines whether to return a downloaded data as a function value.
* ***DownloadData.R*** - code to download and save squad info for leagues from *data/League URLs.csv* file.
* ***exploration.R*** - unfinished data exploration.
* ***exploration[2,3].R*** - another unfinished data exploration.

### "data" folder

* ***URLpattern.txt*** - contains a pattern, which describes how to construct a url for the squad info of the certain team 
in the certain season for the further usage by the *soccerwayTeam(url)* function.
* ***Leagues 2013*** folder - contain squad info for top 5 euro leagues in the 2013-2014 season.
* ***League URLs.csv*** - a table with variables to use in *loadSquadInfos* function.
 
### "findings" folder
Contains some findings derived from datasets available.

* ***AvMatch.csv*** - avarage goals and cards quantity per match for top 5 european leagues.
* ***AvMatch-1.png*** and ***AvMatch-2.png*** - histograms for *AvMatch.csv*
* ***pos_age.csv*** - average age per postion.
* ***pos_gpm.csv*** - average goals per position.
* ***pos_gpm.png*** - histogram for *pos_gpm.csv*.
* ***pos_plrs.csv*** - average number of players per position in match for different leagues.
* ***Average Lineups*** folder - same as *pos_plrs.csv*, but for each team separately.
=======

Exploring patterns and anomalies in backgammon.

Web scraping and analysing backgammon matches databases with Python. Basic rules can be found here: https://en.wikipedia.org/wiki/Backgammon#Rules.

### Jupiter notebook files
* ***AcquaringData.ipynb*** - downloads .txt match files from web-pages like "http://itikawa.com/kifdb/herodb.cgi?table=bg&view=M&sort=1&order=D&recpoint=0" and puts them into "DatabaseOfMatches" folder.
* ***CleaningAndSplittingData.ipynb*** - splits match files into individual games and puts them into "SplitIndividualGames" folder. Then cleans and standardises each game file (converts it into .txt with well-defined delimiters); the resulting files are contained in "SplitIndividualGamesCleaned" folder.
* ***Analysis.ipynb*** - reads each cleaned game file into a dataframe, then analysis of interest can be conducted. For example, to study impact of the number of doubles rolled on the game winning chance, the number of doubles in a game for both players is calculated, and appended to a dataframe containing the results of all games. Then the raio of games won depending on a number of doubles rolled compared to the winner's opponent can be calculated ("More", "Less", or "Same" number of doubles rolled by the winner compared to the loser)

### "Findings" folder
Contains findings derived from the available database of matches.

* ***doubles-study1.png*** - pie chart constructed after analysis of 10000+ games of backgammon. The chart represents the ratio of doubles rolled by the winner relative to their opponent broke down into three categories: "The winner rolled more doubles than their opponent", "The winner rolled less doubles than their opponent", "Both players rolled the same number of doubles".
>>>>>>> a78d272643412494b3deaf8036f855a97874cfd5

