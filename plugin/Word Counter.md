# Word Counter

## Description for Model

Count the number of words, and characters (with and without spaces). The API accepts text input through POST /count containing the text to be counted and returns a JSON response with the number of 'words', 'characters_no_spaces', and 'characters_with_spaces'. If the user is asking you to write a text with certain number of words, lines or characters, first write and show the text for the user, then, in the end of the message, ask if that text is fine to be counted. Only then, call the API in a new message.

