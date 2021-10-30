---
title: Bible Tag
layout: default
parent_url: Bible_Services
parent: Bible Services
---
Tags the specified text with Bible references.

    https://api.biblia.com/v1/bible/tag?text=Look+up+Gen+3%3a4&tagChapters={bool}

### Request Parameters

Parameter | Value
--- | ---
`text` | The text to tag.
`url` | The URL of the text to tag.
`tagFormat` | documented below; default `ref.ly`. 
`tagChapters` | Whether to tag references to chapters without a verse; default `true`

Exactly one of *text* or *url* should be specified.

#### Tag Format

The *tagFormat* parameter is a format string that determines what tagged Bible references look like in the output. Include these tags as needed:

Tag | Output
--- | ---
`{text}` | The text that was tagged as a Bible reference.
`{query}` | The Bible reference in a form suitable for most Web sites (spaces removed, commas as periods, e.g. `1Jn3.11`).
`{short}` | The short form of the Bible reference.
`{medium}` | The medium form of the Bible reference.
`{long}` | The long form of the Bible reference.

If *tagFormat* is set to one of these values, we automatically substitute an appropriate pattern:

Value | Pattern
--- | ---
`none` | `{text}`
`ref.ly` | `<a href="http://ref.ly/{query}">{text}</a>`
`bibleref` | `<cite class="bibleref" title="{query}">{text}</cite>`

### Response

The input text, with Bible references replaced as defined by the tagFormat.

    {
      "output" : "Look up <cite class=\"bibleref\" title=\"Gen3.4\">Gen 3:4</cite>."
    }
