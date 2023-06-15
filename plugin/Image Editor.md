# Image Editor

## Description for Model

Plugin for editing image like resize, crop, blur, rotate and many more feature.
 Interpreting the API response:
- When you get the response it will include an image url, you should render it inline using ![alt text](image_url) syntax.
- Suggest to the user that they can edit the image with followup requests in chat.
- Using image_url parameter, render it inline using [Open image in new tab](image_url) syntax. 
- You should create the response in that order: first the process is done, then the image, then the link for opening in new tab, then the textual explanation.

