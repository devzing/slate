---
title: Swyfft Partner API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - csharp
  - php

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - quote
  - address
  - widget
  - errors

search: true
---

# Swyfft Partner API

###Who do I talk to?

If you have questions about how to use the Swyfft Partner API, contact Ken Smith (ken@swyfft.com), Casey Webster (casey@swyfft.com), Wayne Allen (wayne@swyfft.com) or Sergiy Zinovyev (sergiy@swyfft.com).

### REST API overview

The Swyfft Partner API uses HTTP methods and a RESTful endpoint structure. The API authentication framework is based on API key. Requests and responses have JSON-formatted data.

Use the Swyfft REST APIs in these environments:

* **Sandbox/Test** Use your test `SwyfftApiKey` sent to you to make calls to the Sandbox URI: <https://swyfftbeta.azurewebsites.net/partnerapi/v1>
* **Live/Production** Use your production `SwyfftApiKey` sent to you to make calls to the Live/Production URI: <https://swyfft.com/partnerapi/v1>

**Note:** Swyfft uses secure HTTPS protocol and it replies with HTTP 403 (Forbidden) "SSL Required" when HTTP is used.

To construct a REST call, combine:

* The HTTP method
* The full URI to the resource
* HTTP headers
* The JSON-formatted payload

### Widget

Swyfft also provides a simple, easy-to-use widget that you can load onto your website with as little as two lines of code. See the [Widget](#Widget) page for more details.

# Authentication

Swyfft uses API keys to allow access to the API.

Swyfft expects the API key to be included in all API requests to the server in a header that looks like the following:

`X-SwyfftApiKey: SwyfftApiKey`

<aside class="notice">
You must replace <code>SwyfftApiKey</code> with your personal API key.
</aside>

**Note:** `SwyfftApiKeys` are different for Test and Production environments and sent separately to you.

If authentication fails an **HTTP 401** is returned with an error response in the body.

`
{
  "StatusCode": 1010,
  "Error": {
    "Code": 1010,
    "Message": "Unrecognized api key."
  }
}
`