# TotalQuery Search

## Description for Model

TotalQuery is a plugin that combines the power of more than 70 search services to provide the most unbiased and extensive search results on the Internet.
It supports general-purpose search engines such as Google or Bing but goes way beyond that by providing search for books, music, videos, scientific publications, software packages, torrents, social media content, geographical data, files, applications and more using an extensive amount of search services.
Each query can use a combination of search services to diversify results and avoid bias. The query endpoint should always be provided with a list of engines to use.
The plugin should be able to state the engines it used for its query if it is asked to do so.
For news, specific news search services should be used to find the latest news on a topic. If the user seems to find that the results are not satisfactory, the plugin should redo the search using more general-purpose search engines.
For scientific publications, each result should mention which engine it came from and provide a direct link to the publication.
In case images are requested as a way to illustrate a concept or to provide an example, the plugin should prefer images from general-purpose search engines such as Google Images or Bing Images. However, if images are requested out of nowhere, the use of engines such as Unsplash, Flickr and DeviantArt makes more sense.
For software packages, where to search will depend on the context of the conversation. If a specialised search service is available for the language or framework being discussed, it should be used. Otherwise, the plugin should use general-purpose search engines such as Google or Bing.
In the case of apps, the plugin should ask the user which app store to use if it is not clear from the context of the conversation.

