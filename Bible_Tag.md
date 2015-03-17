---
title: Biblia.com API Documentation
layout: default
---
[Bible Services](Bible_Services) >

# Bible Tag

Tags the specified text with Bible references.

```
https://api.biblia.com/v1/bible/tag?text=Look+up+Gen+3:4
```

### Request Parameters

<table>
<tr><td> text </td><td> The text to tag. </td></tr>
<tr><td> url </td><td> The URL of the text to tag. </td></tr>
<tr><td> tagFormat </td><td> documented below; default ref.ly </td></tr>
</table>

Exactly one of *text* or *url* should be specified.

#### Tag Format

The *tagFormat* parameter is a format string that determines what tagged Bible references look like in the output. Include these tags as needed:

<table>
<tr><td> {text} </td><td> The text that was tagged as a Bible reference. </td></tr>
<tr><td> {query} </td><td> The Bible reference in a form suitable for most Web sites (spaces removed, commas as periods, e.g. `1Jn3.11`). </td></tr>
<tr><td> {short} </td><td> The short form of the Bible reference. </td></tr>
<tr><td> {medium} </td><td> The medium form of the Bible reference. </td></tr>
<tr><td> {long} </td><td> The long form of the Bible reference. </td></tr>
</table>

If *tagFormat* is set to one of these values, we automatically substitute an appropriate pattern:

<table>
<tr><td> none </td><td> `{text}` </td></tr>
<tr><td> ref.ly </td><td> `<a href="http://ref.ly/{query}">{text}</a>` </td></tr>
<tr><td> bibleref </td><td> `<cite class="bibleref" title="{query}">{text}</cite>` </td></tr>
</table>

### Response

The input text, with Bible references replaced as defined by the tagFormat.

```
{
  "output" : "Look up <cite class=\"bibleref\" title=\"Gen3.4\">Gen 3:4</cite>."
}
```
