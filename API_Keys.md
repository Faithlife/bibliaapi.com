---
title: API Keys
layout: default
---

API keys allow you to access the Biblia.com services.


## Getting an API Key

Sign in to [https://api.biblia.com/v1/Users/SignIn](https://api.biblia.com/v1/Users/SignIn). From here you can manage your API keys. An API key may only be used by a single application, so you will need to register for a new one for each web site or application you develop.

## Using your API Key

The API key must be provided in every request made to the Biblia.com services through the `key` parameter.

    https://api.biblia.com/v1/bible/find?key=abc123

### Web sites

Web sites using the Biblia.com API are required to provide the URL of the project. In many cases web sites are unable to conceal the API key. For this reason, the API key registered for this application will only function from web pages hosted under the URL you provide. `localhost` is also accepted, allowing you to use the same API key during development.

## Restrictions

Every application or web site using the Biblia.com services must use its own API key. **Do not** share your API key with anyone. API keys used for more than one project may be disabled without warning.


**Usage of a Biblia.com API key indicates your acceptance of the [Terms of Use](Terms_of_Use).**
