# bg-mining
Exploring patterns and anomalies in backgammon
# bg-mining
Exploring patterns and anomalies in backgammon
=========

Web scraping and analysing backgammon matches databases with Python. Basic rules can be found here: https://en.wikipedia.org/wiki/Backgammon#Rules.

### Jupiter notebook files
* ***AcquaringData.ipynb*** - downloads .txt match files from web-pages like "http://itikawa.com/kifdb/herodb.cgi?table=bg&view=M&sort=1&order=D&recpoint=0" and puts them into "DatabaseOfMatches" folder.
* ***CleaningAndSplittingData.ipynb*** - splits match files into individual games and puts them into "SplitIndividualGames" folder. Then cleans and standardises each game file (converts it into .txt with well-defined delimiters); the resulting files are contained in "SplitIndividualGamesCleaned" folder.
* ***Analysis.ipynb*** - reads each cleaned game file into a dataframe, then analysis of interest can be conducted. For example, to study impact of the number of doubles rolled on the game winning chance, the number of doubles in a game for both players is calculated, and appended to a dataframe containing the results of all games. Then the raio of games won depending on a number of doubles rolled compared to the winner's opponent can be calculated ("More", "Less", or "Same" number of doubles rolled by the winner compared to the loser)

### "Findings" folder
Contains findings derived from the available database of matches.

* ***doubles-study1.png*** - pie chart constructed after analysis of 10000+ games of backgammon. The chart represents the ratio of doubles rolled by the winner relative to their opponent broke down into three categories: "The winner rolled more doubles than their opponent", "The winner rolled less doubles than their opponent", "Both players rolled the same number of doubles".

