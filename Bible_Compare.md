---
title: Bible Compare
layout: default
---
[Bible Services](Bible_Services) >

Compares two Bible references.

```
https://api.biblia.com/v1/bible/compare?first={bible reference}&second={bible reference}
```

### Examples

[https://api.biblia.com/v1/bible/compare?first=Ge+3:4&second=Ge+3:1-10&key=abc123](https://api.biblia.com/v1/bible/compare?first=Ge+3:4&second=Ge+3:1-10&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

### Request Parameters

<table>
<tr>
<td>first</td>
<td>The first Bible reference to compare.</td>
</tr>
<tr>
<td>second</td>
<td>The second Bible reference to compare.</td>
</tr>
</table>

### Response

```
{
  "equal" : (true/false),
  "intersects" : (true/false),
  "compare" : (-1/0/1),
  "startToStart" : (-1/0/1),
  "startToEnd" : (-1/0/1),
  "endToStart" : (-1/0/1),
  "endToEnd" : (-1/0/1),
  "after" : (true/false),
  "before" : (true/false),
  "subset" : (true/false),
  "strictSubset" : (true/false),
  "superset" : (true/false),
  "strictSuperset" : (true/false),
}
```
