---
title: Biblia.com API Documentation
layout: default
---
# Bible Services

## Available Services

| Service Name | Description |
| - | - |
| [Content](Bible_Content) | Returns the content of a Bible. |
| [Table of Contents](Table_of_Contents) | Returns the table of contents of a Bible. |
| [Search](Bible_Search) | Searches the text of a Bible, optionally using a "fuzzy search" algorithm. |
| [Find](Bible_Find) | Finds one or more Bibles and provides Bible metadata. |
| [Image](Bible_Image) | Returns the cover image for a Bible. |
| [Parse](Bible_Parse) | Parses the specified text as one or more Bible passages. Can also be used to render a Bible reference in short, medium, or long form. |
| [Scan](Bible_Scan) | Scans the specified text for Bible references. |
| [Tag](Bible_Tag) | Tags the specified text with Bible references. |
| [Compare](Bible_Compare) | Compares two Bible references. |


## HTTP

The Biblia.com API can be accessed with basic HTTP requests. Unless otherwise specified, all services support both GET and POST.

## Common Parameters

Each service supports a number of parameters, documented in the *Request Parameters* table of each service's page.

In addition to the service-specific parameters, the following parameters can be used with all services.

#### API Key

Every service call requires the API key to be provided in the `key` parameter. See [API Keys](API_Keys) for more information.

#### Culture

The user's culture can be provided with the `culture` parameter. If a `culture` parameter is not found, the `Accept-Language` HTTP header will be used. If neither of those are found, `en-US` will be used. The culture is used by some services to decide how to parse Bible references, for example. Unsupported cultures will fall back to the closest available culture, or en-US.

#### Output Format

Most services support a number of different output formats. Please see the [Output Format](Output_Format) page for details.

## Available Bibles

See the [Available Bibles](Available_Bibles) page for details.
