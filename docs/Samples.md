---
title: Samples
layout: default
---

## Request Samples

The following examples demonstrate how to use various services.

These samples use "abc123" in place of a real [API key](API_Keys).

#### Get a list of all available Bibles and their metadata in JSON or XML format

[https://api.biblia.com/v1/bible/find?key=abc123](http://api.biblia.com/v1/bible/find.txt?key=fd37d8f28e95d3be8cb4fbc37e15e18e)

[https://api.biblia.com/v1/bible/find.xml?key=abc123](http://api.biblia.com/v1/bible/find.xml?key=fd37d8f28e95d3be8cb4fbc37e15e18e)

#### Get the plain text of John 3:16 from the LEB with JSONP

[https://api.biblia.com/v1/bible/content/LEB.txt.js?passage=John3.16&callback=myCallbackFunction&key=abc123](http://api.biblia.com/v1/bible/content/LEB.txt.txt?passage=John3.16&callback=myCallbackFunction&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

#### Get HTML for John 3 from the LEB

[https://api.biblia.com/v1/bible/content/LEB.html?passage=John3&style=fullyFormatted&key=abc123](http://api.biblia.com/v1/bible/content/LEB.html?passage=John3&style=fullyFormatted&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

#### Search the LEB for "bread", and return the top 20 results in JSON format

[https://api.biblia.com/v1/bible/search/LEB.js?query=bread&mode=verse&start=0&limit=20&key=abc123](http://api.biblia.com/v1/bible/search/LEB.txt?query=bread&mode=verse&start=0&limit=20&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

#### Parse "II Kgs 1:1-2, 3-5" into Bible references, rendering them in short format

[https://api.biblia.com/v1/bible/parse.js?passage=II Kgs 1:1-2, 3-5&style=short&key=abc123](http://api.biblia.com/v1/bible/parse.txt?passage=II Kgs 1:1-2, 3-5&style=short&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

[https://api.biblia.com/v1/bible/parse.js?passage=2 Reyes 1:1-2, 3-5&culture=es&style=short&key=abc123](http://api.biblia.com/v1/bible/parse.txt?passage=2 Reyes 1:1-2, 3-5&culture=es&style=short&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

#### Locate Bible references in the text "My favorite Bible verse is Jn 3:16. John 3:17 is good too."

[https://api.biblia.com/v1/bible/scan.js?text=My favorite Bible verse is Jn 3:16. John 3:17 is good too.&key=abc123](http://api.biblia.com/v1/bible/scan.txt?text=My favorite Bible verse is Jn 3:16. John 3:17 is good too.&key=fd37d8f28e95d3be8cb4fbc37e15e18e)
