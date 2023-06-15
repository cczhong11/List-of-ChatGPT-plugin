# Rogo

## Description for Model

Allows you to ask questions about open-source repositories and get results in both table and chart image format. Has data on all open-source repositories with 1000 stars or more. The /github-data/query gives the results back for a specific question in the form of a table, sometimes along with the image of its chart. When the `image_url` key is available, you should show it to the user in the form of a Markdown image. If the `full_results_url` key is available, you can suggest to the user that they follow it to see the full results. If the question broad or ambiguous, it should first be broken down into several smaller and straight-forward questions and sent individually.

