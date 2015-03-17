---
title: Biblia.com API Documentation
layout: default
---
# Output Format

Unless otherwise specified, all services use [JSON](http://json.org/) by default.

To change the output format, add a "file extension". For example, `…/find` returns JSON, but `…/find.xml` returns XML (documented below).

Some services (such as the [Content](Bible_Content) service) can provide data that isn't "wrapped" in JSON or XML. In those cases, the file extension indicates the output format (e.g. `.txt` or `.html`). To wrap that content in JSON or XML, you can supply another extension (e.g. `.html.json`, which returns the HTML wrapped in a JSON object with an "html" property).

For purposes of debugging, any service that returns JSON can also return text, which returns nicely-formatted JSON (e.g. `…/find.txt` returns pretty JSON).

## JSONP Support

When requesting `json`, a `callback` parameter can be supplied to transform the response into [JSONP](https://en.wikipedia.org/wiki/JSON#JSONP) format, allowing JavaScript applications to place cross-domain requests. A `requestId` parameter can optionally be used to supply a second parameter to the JSONP callback.

## XML

Our XML format is a predictable transformation from the JSON format. The root element is always `<response>`.

### Example JSON document

```
{
  "name" : "Joe",
  "age" : 34,
  "ratio" : 0.75,
  "male" : true,
  "birthplace" : {
    "city" : "Bellingham",
    "state" : "WA"
  },
  "children" : [
    "Manny",
    "Moe",
    "Jack"
  ]
}
```

### Example XML document

```
<response>
  <name>Joe</name>
  <age>34</age>
  <ratio>0.75</ratio>
  <male>true</male>
  <birthplace>
    <city>Bellingham</city>
    <state>WA</state>
  </birthplace>
  <children>Manny</children>
  <children>Moe</children>
  <children>Jack</children>
</response>
```
