---
title: Bible Scan
layout: default
parent_url: Bible_Services
parent: Bible Services
---
Scans the specified text for Bible references.

    https://api.biblia.com/v1/bible/scan/?text={text}&tagChapters={bool}

### Example

[https://api.biblia.com/v1/bible/scan?text=Look+at+Gen+1:1&key=abc123](https://api.biblia.com/v1/bible/scan?text=Look+at+Gen+1:1&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

### Request Parameters

<table>
<tr><td> text </td><td> The text to parse (required). </td></tr>
<tr><td> tagChapters </td><td> Whether to tag references to chapters without a verse; default <code>true</code>. </td></tr>
</table>

### Response

    {
      "results" : [
        {
          "passage" : "Genesis 3:4",
          "textIndex" : (index into text, eg: 8 ),
          "textLength" : (length of parsed reference text, eg: 7)
        },
        …
      ]
    }
