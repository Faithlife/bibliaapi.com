---
title: Bible Content
layout: default
---
[Bible Services](Bible_Services) >

Returns the content of a Bible.

    https://api.biblia.com/v1/bible/content/{bible}.{outputFormat}?passage={bibleReference}&key={API key}

### Example

[https://api.biblia.com/v1/bible/content/LEB.html?passage=John3.16&key=abc123](https://api.biblia.com/v1/bible/content/LEB.html?passage=John3.16&key=fd37d8f28e95d3be8cb4fbc37e15e18e)

### Request Parameters

<table>
<tr><td> bible </td><td> The ID of the Bible (required). </td></tr>
<tr><td> passage </td><td> The Bible passage to return (required). </td></tr>
<tr><td> outputFormat </td><td> Content type returned (options below) </td></tr>
<tr><td> style </td><td> The name of a pre-defined style (options below). **Note: Takes precedence over the more specific options e.g. redLetter, header** </td></tr>
<tr><td> formatting </td><td> all, paragraph, character, or none. Default all </td></tr>
<tr><td> redLetter </td><td> false to remove red letter formatting for words of Christ. Default true. </td></tr>
<tr><td> footnotes </td><td> true to include footnote content below the main content; default false. </td></tr>
<tr><td> citation </td><td> true to include a citation below the content; default false. </td></tr>
<tr><td> paragraphs </td><td> true to preserve paragraphs, false for one verse per line; default true. </td></tr>
<tr><td> fullText </td><td> true to include everything, not only the biblical text; default false. </td></tr>
<tr><td> header </td><td> format of the header (see blow); default empty </td></tr>
<tr><td> eachVerse </td><td> format of the footer; default [VerseText] </td></tr>
<tr><td> footer </td><td> format of the footer; default empty </td></tr>
</table>

#### Output formats

The supported output formats are text (`.txt`) and HTML (`.html`). To wrap the output in a JSON object, add a `.json` extension (e.g. `.html.json`).

#### Available pre-defined styles

NOTE: These styles correspond to the default Logos 4 Copy Bible Verses styles.

* fullyFormatted
* oneVersePerLine
* oneVersePerLineFullReference
* quotation
* simpleParagraphs
* bibleTextOnly
* orationOneParagraph
* orationOneVersePerLine
* orationBibleParagraphs
* fullyFormattedWithFootnotes

#### Formatting headers, footers, and verse content

These parameters use the Logos 4 Copy Bible Verses syntax. Additional documentation and examples can be found in the Logos 4 help.

##### Replacement tokens

<table>
<tr><td> [FullPassageRef] </td><td> e.g., John 3:16-18 </td></tr>
<tr><td> [ShortPassageRef] </td><td> e.g., Jn 3:16-18 </td></tr>
<tr><td> [FullBookName] </td><td> e.g., John </td></tr>
<tr><td> [ShortBookName] </td><td> e.g., Jn </td></tr>
<tr><td> [ChapterNum] </td><td> e.g., 3 </td></tr>
<tr><td> [VerseNum] </td><td> e.g., 16 </td></tr>
<tr><td> [FullVerseRef] </td><td> e.g., John 3:16 </td></tr>
<tr><td> [ShortVerseRef] </td><td> e.g., Jn 3:16 </td></tr>
<tr><td> [Version] </td><td> e.g., ESV </td></tr>
<tr><td> [VerseText] </td><td> e.g., For God so loved … </td></tr>
</table>

##### Examples

Format headers with the verse reference and Bible version, in its own paragraph:

    [FullPassageRef] ([Version])
