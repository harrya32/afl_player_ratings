# afl_player_ratings

The AFL is quite possibly the [most data-rich sport in the world](https://www.vice.com/en_au/article/mg83jy/analytics-in-the-afl-the-most-data-rich-sport-on-earth), given the number of players on the field at any one time (18 for each team), and the narrow restrictions on how each player can affect the game state.

While a lot of this data is kept behind closed doors, unavailable to the public, there are still a substantial number of stats tracked for each player which are released to everyone, and quite often these stats are referred back to by many in the community to demonstrate how well, or poorly, a player played for a specific match.

Through my analysis of some of this available data, I hope to see whether these stats can paint a true picture of player and team performance, or whether it is not possible to properly judge a game without having seen it. The stats don't lie... or do they?

## Data
The data I have based my project on is sourced from [MichaelStone's Kaggle](https://www.kaggle.com/stoney71/aflstats). It tracks many stats for each player in each game from 2012 - 2018. I have made use of the following stats:
* Player name
* Season
* Round
* Game margin
* Opposition
* Disposals
* Kicks
* Marks
* Handballs
* Goals
* Behinds
* Hitouts
* Tackles
* Rebound 50s
* Inside 50s
* Clearances
* Clangers
* Frees for
* Frees against
* Brownlow votes
* Contested possessions
* Uncontested possessions
* Contested marks
* Marks inside 50
* One percenters
* Bounces
* Goal assists
* Percent played

## Rating system
Using these stats, I endeavoured to make a player rating system, similar to what has been done with AFL fantasy or supercoach points, in order to be able to grade each player's overall game. To do this, I first calculated the correlations between each in-game stat and the overall game margin, to essentially grade the worth of each stats. I then used these correlations to weight how important each stat was — the higher the correlation, the more important as, in general, if a player got a lot of that specific stat, their team's margin would improve.
