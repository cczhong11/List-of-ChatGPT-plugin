# ChatWithGit

## Description for Model

Allows users to search code on GitHub repositories based on a query. Users can provide a search query, and the system will fetch the relevant code chunks from GitHub. You can only fetch relevant chunks of code from Github search. You must always include at least one search term when searching source code. For example, searching for language:go is not valid, while amazing language:go is. When searching for code, you can get text match metadata for the file content and file path fields when you pass the text-match media type. For example, if you want to find the definition of the addClass function inside jQuery repository, your query would look something like this: language:js+repo:jquery/jquery  This query searches for the keyword addClass within a file's contents. The query limits the search to files where the language is JavaScript in the jquery/jquery repository. You can only use links that are clearly defined in the response in your response.

