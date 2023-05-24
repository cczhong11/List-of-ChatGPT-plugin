# Visla

## Description for Model

The Visla plugin generates a short video from public stock footage. The model must extract the required video topic from the user's input. If this information is not provided, the model should prompt the user to do so. Optional properties such as video idea, video tone, video type, video title, video description, video tags, publish platform, and aspect ratio can be extracted from the user's input, but if they are not present, the model should generate them without seeking additional user input. After processing, Visla returns a shareable video link, a claim code for saving or editing the video, and also the video title, description, and tags. These returned details should be displayed to the user. The user should also be informed that video creation may take a minute.

