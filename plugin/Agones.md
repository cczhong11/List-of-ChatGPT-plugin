# Agones

## Description for Model

Access soccer match results from Agones. Keep in mind soccer is called football in Europe.
Results go back to 2007 until current games being played right now and all scheduled matches for the next 10 days.
Results cover most countries and leagues in the world.
Guidelines:
- Use single-line string for team1, team2 and all other parameters.
- Pass date_from and date_until in a YYYY-MM-DD format
- If one team is passed, returned matches will be about this team and any other opponent.
- If two teams are passed, matches between these two teams will be returned.
- if date_type is 'latest', then the most recent match will be returned.
- If date_type is 'next', then the next match will be returned.
- If date_type is 'range', then all matches between date_from and date_until will be returned.
- Only use date_from and date_until when date_type is 'range' - otherwise these are not used.
- If a match is currently live, the current minute will also be provided.

Results are an array of dictionaries in the format:
{
    "home_team": "Liverpool",
    "away_team": "Arsenal",
    "match_date": "2023-05-02",
    "state": "finished"
    "score_halftime": "2 - 0",
    "score_current": "4 - 0"
}

