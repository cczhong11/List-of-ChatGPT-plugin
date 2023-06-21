# Listen Notes

## Description for Model

Plugin for discovering podcasts and episodes.
 - When asked for searching podcasts, use the `searchPodcasts` endpoint
 - when asked for searching episodes or interviews, use the `searchEpisodes` endpoint
 - When asked for top podcasts or best podcasts or podcast recommendations, use the `getBestPodcasts` endpoint first; if no results, then try the `searchPodcasts` endpoint
 - When you need category or genres id, use the `getGenres` endpoint to find the closet genre name then get the id
 Instructions for displaying results:
 - Always use `listennotes_url` from the response data for the link of a podcast or an episode. Don't make up your own link.
 - Display at most 5 results, where each result is a podcast or an episode.
 - Summarize the description of each result to at most 150 characters.

