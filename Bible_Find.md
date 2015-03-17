---
title: Bible Find
layout: default
---
[Bible Services](Bible_Services) >

Finds one or more Bibles.

    https://api.biblia.com/v1/bible/find/{bible}
    
    https://api.biblia.com/v1/bible/find?query={query}

### Examples

Both of the following requests will return information for the Lexham English Bible (LEB).

[https://api.biblia.com/v1/bible/find?query=lexham&key=abc123](https://api.biblia.com/v1/bible/find?query=lexham&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

[https://api.biblia.com/v1/bible/find/leb.json?key=abc123](https://api.biblia.com/v1/bible/find/leb.json?key=fd37d8f28e95d3be8cb4fbc37e15e18e)

The following request will return *all* available Bibles.

[https://api.biblia.com/v1/bible/find?key=abc123](https://api.biblia.com/v1/bible/find?key=fd37d8f28e95d3be8cb4fbc37e15e18e)

### Request Parameters

Only Bibles that match **all** of the request parameters will be returned. If no request parameters are specified, all entries are returned.

<table>
<tr><td> bible </td><td> The ID of the Bible (e.g. "KJV"). </td></tr>
<tr><td> query </td><td> The query that matches the Bibles to return. </td></tr>
<tr><td> strictQuery </td><td> The strict query (words only match title, abbreviation, and author) that matches the Bibles to return. </td></tr>
<tr><td> start </td><td> The zero-based index of the first entry to return (default 0). </td></tr>
<tr><td> limit </td><td> The maximum number of entries to return (all if unspecified). </td></tr>
</table>

### Response

    {
      "bibles" : [
        {
          "bible" : …,
          "title" : …,
          "abbreviatedTitle" : …,
          "publicationDate" : …,
          "languages" : […],
          "publishers" : […],
          "imageUrl" : …,
          "description" : …,
          "copyright" : …,
          "extendedCopyright" : …
        },
        …
      ]
    }
