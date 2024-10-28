# Yahoo-Fantasy-League-Stats
Script designed to automatically help fantasy sports enthusiasts pull and analyze team and player stats for their Head to Head Yahoo NBA fantasy league based off 2025 player projections.

Player information is pulled from the "Starting Rosters" section of a Yahoo NBA Fantasy League, then merged with 2025 player projections from hashtagbasketball.com.

Team stats are evaluated using Z scores (standard deviations from the mean) for each category for each player. The script creates an excel file with a sheet for each team containing their player's stats and zscores (along with a few other things). It also creates a sheet summarizing each team's rating for each category.

![image](https://github.com/user-attachments/assets/d3ac8550-8bf1-4a8d-831c-19750dffe811)

![image](https://github.com/user-attachments/assets/affb1098-3aea-42dc-bb0d-c94e61f07426)


## How it works
Libraries: pandas, request, bs4, selenium, io, fuzzywuzzy, time

1. Extract Team info from Yahoo League Rosters site.
2. Extract player stat projections for all NBA players from hashtag basketball using selenium webdriver.
3. Convert to data frames and merge (using fuzzywuzzy to account for errors due to slight differences such as nicknames)
4. Calculate Z values and any additional information (as well as team totals).
5. Save to multiple Excel sheets for ease of viewing.





Things to work on:
- Change FG% and FT% to accurately reflect player's shot attempts. (Players may shoot 100% but if they take very few shots a game it won't have much of an effect.)
- More helpful data visualizations.
