---
title: Echonio API Reference

language_tabs:
  - curl

toc_footers:

includes:
  - tokens
  - customers
  - contacts
  - departments
  - operators
  - files
  - tasks
  - timeline-events
  - settings
  - errors

search: true
---

# Introduction

The Echonio API is organized around REST. Our API has predictable, resource-oriented URLs, and uses HTTP response codes to indicate API errors. We use built-in HTTP features, like HTTP authentication and HTTP verbs, which are understood by off-the-shelf HTTP clients. We support cross-origin resource sharing, allowing you to interact securely with our API from a client-side web application (though you should never expose your secret API key in any public website's client-side code). JSON is returned by all API responses, including errors.

# Authentication

> To authorize, use this code:

```curl
curl https://api.echon.io/v1/customers
  -H "Authorization: meowmeowmeow"
```

> Make sure to replace `meowmeowmeow` with your API key.

Echonio uses API keys to allow access to the API. You can register a new API key at our [developer portal](http://api.echon.io/).

Echonio expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

