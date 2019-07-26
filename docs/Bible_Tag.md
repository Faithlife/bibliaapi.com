---
title: Bible Tag
layout: default
parent_url: Bible_Services
parent: Bible Services
---
Tags the specified text with Bible references.

    https://api.biblia.com/v1/bible/tag?text=Look+up+Gen+3%3a4&tagChapters={bool}

### Request Parameters

<table>
<tr><td> text </td><td> The text to tag. </td></tr>
<tr><td> url </td><td> The URL of the text to tag. </td></tr>
<tr><td> tagFormat </td><td> documented below; default ref.ly. </td></tr>
<tr><td> tagChapters </td><td> Whether to tag references to chapters without a verse; default <code>true</code>. </td></tr>
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
<tr><td> none </td><td> <code>{text}<code> </td></tr>
<tr><td> ref.ly </td><td> <code>&lt;a href="http://ref.ly/{query}"&gt;{text}&lt;/a&gt;</code> </td></tr>
<tr><td> bibleref </td><td> <code>&lt;cite class="bibleref" title="{query}"&gt;{text}&lt;/cite&gt;</code> </td></tr>
</table>

### Response

The input text, with Bible references replaced as defined by the tagFormat.

    {
      "output" : "Look up <cite class=\"bibleref\" title=\"Gen3.4\">Gen 3:4</cite>."
    }
