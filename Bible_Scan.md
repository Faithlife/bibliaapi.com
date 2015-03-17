---
title: Bible Scan
layout: default
---
[Bible Services](Bible_Services) >

Scans the specified text for Bible references.

```
https://api.biblia.com/v1/bible/scan/?text={text}
```

### Example

[https://api.biblia.com/v1/bible/scan?text=Look+at+Gen+1:1&key=abc123](https://api.biblia.com/v1/bible/scan?text=Look+at+Gen+1:1&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

### Request Parameters

<table>
<tr><td> text </td><td> The text to parse (required). </td></tr>
<tr><td> style </td><td> Style of the rendered form (short, medium, long, display; default long). </td></tr>
</table>

### Response

```
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
```
