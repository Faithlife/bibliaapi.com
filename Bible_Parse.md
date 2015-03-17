---
title: Bible Parse
layout: default
---
[Bible Services](Bible_Services) >

Parses the specified text as one or more Bible passages. Can also be used to render a Bible reference in short, medium, or long form.

```
https://api.biblia.com/v1/bible/parse
```

### Examples

[https://api.biblia.com/v1/bible/parse?passage=2+Kgs+3-4&key=123abc](https://api.biblia.com/v1/bible/parse?passage=2+Kgs+3-4&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

[https://api.biblia.com/v1/bible/parse?passage=2+Kgs+1-2,+4-5&key=123abc](https://api.biblia.com/v1/bible/parse?passage=2+Kgs+1-2,+4-5&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

### Request Parameters

<table>
<tr><td> passage </td><td> The text to parse (required). </td></tr>
<tr><td> style </td><td> Style of the rendered form (short, medium, long; default long). </td></tr>
</table>

### Response

```
{
  "passage" : "2 Kings 3:1-2, 4-5"
  "passages" : [
    {
      "passage" :  "2 Kings 3:1-2",
      "parts" : { "book" : "2 Kings", "chapter" : 3, "verse" : 1, "endVerse" : 2 }
    },
    {
      "passage" : "2 Kings 3:4-5",
      "parts" : { "book" : "2 Kings", "chapter" : 3, "verse" : 4, "endVerse" : 5 }
    }
  ]
}
```
