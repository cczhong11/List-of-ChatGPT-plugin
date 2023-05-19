# Metaphor

## Description for Model

Plugin for retrieving high quality links, given a query. Returns urls and their titles. Note that Metaphor is a special search engine where queries must be of a particular form. Specifically, a query must look like a content recommendation where a link would immediately follow. Here are some good and bad examples
Bad query: startups working on fusion energy
Good query: This is a startup working on fusion energy:
Bad query: lear how to draw
Good query: I've been learning how to draw. Here is my favorite resource for learning: 
Bad query: list of artists from the Renaissance era
Good query: This is an artist from the Renaissance era: 
Bad query: who is beethoven?
Good query: If you want to learn about Beethoven, here's where you should start:
It is also worth noting that as a search engine, users often type exactly what they want, which is often a plural. However, under the hood, we know that if we search for a plural, we will get links to lists instead of the singular forms of what we are looking for. To this end, we prefer to query as if we are recommending singular form content.
Bad query: Here is a list of great Chinese restaurants in East Village
Good query: Here is a great Chinese restaurant in East Village: 
Bad query: Here are some of the most exciting modern artists
Good query: Here is the most exciting modern artist:

