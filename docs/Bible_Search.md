---
title: Bible Search
layout: default
parent_url: Bible_Services
parent: Bible Services
---
Searches the text of a Bible.

    https://api.biblia.com/v1/bible/search/{bible}?query={query}

### Example

[https://api.biblia.com/v1/bible/search/LEB.js?query=bread&mode=verse&start=0&limit=20&key=abc123](https://api.biblia.com/v1/bible/search/LEB.js?query=bread&mode=verse&start=0&limit=20&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

### Request Parameters

<table>
<tr><td> bible </td><td> The ID of the Bible to search (e.g. "KJV"). </td></tr>
<tr><td> query </td><td> The query text. </td></tr>
<tr><td> mode </td><td> verse or fuzzy; default verse. </td></tr>
<tr><td> passages </td><td> The passages to search in (e.g. "Matthew-John"). Only valid with mode=verse. </td></tr>
<tr><td> start </td><td> The zero-based index of the first result to return (default 0). </td></tr>
<tr><td> limit </td><td> The maximum number of results to return (all if unspecified). </td></tr>
<tr><td> preview </td><td> none, text, or html; default text. </td></tr>
<tr><td> sort </td><td> The sort order (relevance or passage). Only valid with mode=verse. mode=fuzzy always sorts by passage. </td></tr>
</table>

### Response

    {
      "results" : [
        {
          "passage" : "John 1:1",
          "preview" : "In the beginning was the Word, and the Word was with God, and the Word was God."
        },
        …
      ]
    }
