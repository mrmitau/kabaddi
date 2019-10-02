# kabaddi
Upgrad Hackathon

## Team
Neophytes

## Team members
Kavitha M S       (Upgrad id = APFE18813692)
Magesh Matapathy  (Upgrad id = APFE18815379)
Anitha Matapathy  (Non-upgrad member)

## Pro Kabaddi Hackathon

## Objective
To predict the following for current season -Season 7, 2019
#### Team
- winner of the tournament
- top team in the points table after the completion of the league matches
- team with the highest points for successful raids
- team with the highest points for successful tackles
- team with the highest super-performance total
#### Players
- player with the highest SUCCESSFUL RAID percentage
- player with the highest SUCCESSFUL TACKLE percentage

#### Data Files Used -
1. Teams_cur_seasons_matches.csv - current seasons completed match details - (Manually collected)
2. Teams_cur_seasons_matches_upcoming.csv - current seasons upcoming match details - (Manually collected)
3. Teams_prev_seasons_matches.csv - scraped -  previous seasons completed match details - (Manually collected)
4. Teams_cur_seasons_allpoints.csv - Current seasons team points scraped - through scripts (source https://www.prokabaddi.com/)
5. Teams_prev_seasons_allpoints.csv - Previous seasons team points scraped through scripts

## Prediction Logic
### Team - Winners/ Top Ranks
- For each season, all match details (teams, winners, match scores, match points, home/away ) and overall, attack and defence points for the season is collected and tabulated for each match
- The team rank pregression with each match is calculated
- The target variable used is 'Team 1 Winner?'
- All completed match data is split into train / test sets.
- Scaled data is used to build a classification model to predict the probability of Team 1 winning
- Using the tuned, final model, the upcoming matches are predicted.
- The team standing ranks are calculated
- the top 3,4,5,6 teams are assigned for elimination matches
- the winners of elimination matches are assigned for semi finals with top 1 and 2 teams
- the finalists are assigned to final match and winner is predicted.
- after each match the team points and ranks are calculated
