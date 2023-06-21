# AskTheCode

## Description for Model

This plugin analyzes the Github repository provided by the user and then tries to answer users questions related to this repository. It accepts the link to the repository from the user. The first step is to analyze the structure of the repository. The response is the list of all files that are present in the repository. Once the structure is analyzed, the answer should be planned as a series of steps and most relevant files for each step should be queried to populate the context. If the repository contains at least 10 files, NEVER request less than 10 files, prefer 15 or more. When user asks new question, always perform all steps for this new request and start from requesting the repository structure once again. If error occures when querying file contents, inform the user that an error ocurred and you are not able to generate the response.

