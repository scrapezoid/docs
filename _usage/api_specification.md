---
layout: page
title: API Specification
nav_order: 2
---

# API Specification

## POST /api/v1/scrape

Fast HTTP mode. Use this endpoint for most use cases, unless you need
Javascript or super stealth mode. The request will act similar to a curl request
but has anti-blocking measures like browser mimicking built in.

Requests to the destination URL is done using HTTP/1.1.

### Request

```json
{
  "url": "https://example.com",
  "method": "GET",
  "headers": {
    "Authorization": "Bearer <token>"
  },
  "data": {
    "key": "value"
  }
}
```

| Parameter  | Description  | Example   | Required    |
|------------|--------------|-----------|-------------|
| `url`      | The destination URL to scrape | `https://example.com` | Yes |
| `method`   | The HTTP method to use | `GET` or `POST` | No |
| `headers`  | HTTP headers to send to the destination URL | `Authorization: Bearer <token>` | No |
| `data`     | The HTTP body to send to the destination URL | `{"key": "value"}` | No |

### Response

```json
{
  "status_code": 200,
  "content_type": "text/html",
  "headers": {
    "server": "nginx",
    "content-length": "123",
    "content-type": "text/html"
  },
  "content": "<html><body>Hello, world!</body></html>"
}
```

## POST /api/v1/scrape/js

Javascript mode. Use this endpoint if you need to scrape websites that use
Javascript to load content. This mode uses a custom headless browser that can
execute Javascript with basic anti-blocking techniques. Some resources like
stylesheets and images are not loaded for performance reasons.

Generally requests to this endpoint will take longer to complete as a fresh
browser session is started, and it's recommended to set a client timeout of at
least 60 seconds.

### Request

```json
{
  "url": "https://example.com"
}
```

## POST /api/v1/scrape/js/super-stealth

Super stealth mode. Use this endpoint if you need to scrape websites that use
Javascript to load content and you're facing more advanced anti-scraping techniques. 
This mode uses a custom headless browser that can execute Javascript with advanced
anti-blocking techniques. Some resources like stylesheets and images are not loaded 
for performance reasons.

Generally requests to this endpoint will take longer to complete as a fresh
browser session is started, captchas may need to be solved during the request, and 
Scrapezoid may retry a request multiple times if it detects that the request was blocked.

### Request

```json
{
  "url": "https://example.com"
}
```


