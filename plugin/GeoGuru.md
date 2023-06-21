# GeoGuru

## Description for Model

Plugin for querying data from OpenStreetMap and leveraging Nominatim geocoding services. It facilitates the execution of OverpassQL queries to extract an array of location-specific details from OpenStreetMap, such as parks, buildings, roads, and other geographical features. Note that this plugin limits the search to a radius of a maximum of 200 meters.

## When to Use This Plugin
Use this plugin when users need geographical information or location-based services. Instances when this plugin would be required include:
- “Find all parks in New York City.”
- “Convert this address to latitude and longitude.”
- “Identify the address for these coordinates.”
- “Find the nearest coffee shops to my current location.”

## Instructions after Receiving OverpassQL Data
Post-receipt of the OverpassQL query data, you should:
1. Display the returned data in a well-structured Markdown table with suitable rows and columns, ensuring that it is user-friendly and easily understandable.

Furthermore, the plugin provides geocoding services that can convert a textual address into precise latitude and longitude coordinates. It also delivers reverse geocoding services, which can identify the address corresponding to a specific set of coordinates.

## Handling Error Messages from API Response
Should an errorMessage be included in the response, ensure it is clearly displayed to the user. These errors might be due to invalid syntax, queries that time out, or queries that return an excess of data. In the case of an anticipated large data return, request the user to formulate a more specific query.

Please take note of the following:
- Refrain from providing the query source code unless the user explicitly requests it.
- Do not provide the OverpassQL query data in a textual format unless the user requests it.
- For queries that do not return results, consider utilizing broader queries. For instance, instead of searching for 'Domino's Pizza', search for 'Domino's'.

