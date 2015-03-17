---
title: Biblia.com API Documentation
layout: default
---
[Bible Services](Bible_Services) >

# Table of Contents

Returns the books and chapters of a given bible version.

```
http://api.biblia.com/v1/bible/contents/{bible}
```

### Example

[https://api.biblia.com/v1/bible/contents/LEB?key=abc123](https://api.biblia.com/v1/bible/contents/LEB?key=fd37d8f28e95d3be8cb4fbc37e15e18e)

### Request Parameters

<table>
<tr><td> bible </td><td> The ID of the Bible (required). </td></tr>
</table>

### Response

```
{
  "books" : [
    {
        "passage" : "Genesis",
        "chapters" : [
            {
              "passage" : "Genesis 1"
            },
            {
              "passage" : "Genesis 2"
            },
            …
        ]
    },
    …
  ]
}
```
