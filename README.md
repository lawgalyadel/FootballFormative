# Formative work

## App Description 

My coursework project is a website where users can choose one of the top five football leagues. After selecting a league, an alphabetically ordered league table of all teams is displayed. Users can then make predictions for individual award winners. Once their predictions are finalized, they can submit them along with their name to a submissions section, where other users can upvote or downvote the predictions.

## API Entities

### League
Attributes: Name, country, teams (a list of teams), etc.
Endpoints:
GET /leagues - Retrieve a list of available leagues.
GET /leagues/{league_id} - Retrieve details of a specific league (including teams).

### Team
Attributes: Name, points, position, and other relevant team stats.
Endpoints:
GET /teams - Retrieve a list of teams across all leagues.
GET /teams/{team_id} - Retrieve specific details about a team.

### Prediction
Attributes: User's name, selected league, predictions for awards (e.g., Player of the Year, Top Scorer), timestamp.
Endpoints:
POST /predictions - Submit a prediction (with name, league, and award predictions).
GET /predictions - Retrieve a list of all submitted predictions.
GET /predictions/{prediction_id} - Retrieve details of a specific prediction.

### Vote
Attributes: User ID, prediction ID, vote type (upvote or downvote), timestamp.
Endpoints:
POST /votes - Submit a vote on a prediction.
GET /votes/{prediction_id} - Retrieve the votes for a specific prediction.