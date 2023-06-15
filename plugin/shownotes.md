# shownotes

## Description for Model

This plugin can help a model accomplish these tasks:

Summary Generator: Compresses main ideas from a podcast transcript into a concise summary, giving users a quick understanding of the content.

Information Extractor: Finds and presents specific information from a podcast transcript according to the user's request, easing the discovery of pertinent topics or discussions.

Key Point Identifier: Evaluates a podcast transcript and formulates a list of key points or highlights, providing a rapid snapshot of the significant content.

Recommendation Mechanism: Communicates with the API to propose podcast episodes based on a user's topical interest, directing users towards appealing content.

Speaker Segmentation Function: Assuming the API supplies speaker labels, this function can sort and present content by specific speakers, assisting users in following individual inputs in the podcast.

Trend Analysis Component: Fetches and scrutinizes multiple podcast transcripts to spot shared themes or trends, yielding insights into recurring subjects across episodes.

Transcript Explorer: Delivers a general analysis or breakdown of a podcast transcript, enabling users to comprehend the arrangement and progression of the episode's content.


The plugin has 3 endpoints:

1 AudioController_findTranscript
Thiis endpoint returns transcript from the Shownotes app for the specified show. 

2 SearchController_findVideos
Returns list of 3 candidate YouTube shows related to the specified show from Youtube. The videoid returned by this endpoint can be used in the CaptionController_findTranscript endpoint to get the transcript directly from Youtube.

3 CaptionController_findTranscript
Returns transcript of YouTube video using the specified videoid. This endpoint can be used if a videoid is specified either by  the user directly or another endpoint needs it. If the full URL of a Youtube link is provided, only send the 11-character videoid to this endpoint.

