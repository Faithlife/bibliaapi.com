---
title: Pericope Search
layout: default
parent_url: Bible_Services
parent: Bible Services
---

Performs a "fuzzy search" of the Bible.

    http://api.biblia.com/v1/bible/pericopesearch/{bible}
    
    http://api.biblia.com/v1/bible/pericopesearch/LEB

### Request Parameters

<table>
<tr><td> bible </td><td> The ID of the Bible to search (e.g. "KJV"). </td></tr>
<tr><td> query </td><td> The query text. </td></tr>
<tr><td> start </td><td> The zero-based index of the first result to return (default 0). </td></tr>
<tr><td> limit </td><td> The maximum number of results to return (all if unspecified). </td></tr>
<tr><td> format </td><td> Output format ([details](Output_Format)). </td></tr>
<tr><td> preview </td><td> none, text, or html; default text. </td></tr>
</table>

### Response
(Same as [Search](Bible_Search))
