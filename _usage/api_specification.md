---
layout: page
title: API Specification
nav_order: 2
---

# API Specification

## Example Request

You can easily make your first API call by using `curl`. Here's an example:

```bash
curl -X POST "https://api.scrapezoid.com/api/v1/scrape" \
     -H "X-Scrapezoid-Auth: YOUR_API_KEY" \
     -H "Content-Type: application/json" \
     -d '{"url": "https://example.com"}'
```

## Endpoints

| Endpoint                          | Description |
|-----------------------------------|-------------|
| POST `/api/v1/scrape`                  | Fast HTTP mode. Use this endpoint for most use cases, unless you need Javascript or super stealth mode. The request will act similar to a curl request but has anti-blocking measures like browser mimicking built in. Requests to the destination URL is done using HTTP/1.1. |
| POST `/api/v1/scrape/js`               | Javascript mode. Use this endpoint if you need to scrape websites that use Javascript to load content. This mode uses a custom headless browser that can execute Javascript with basic anti-blocking techniques. Some resources like stylesheets and images are not loaded for performance reasons. |
| POST `/api/v1/scrape/js/super-stealth` | Super stealth mode. Use this endpoint if you need to scrape websites that use Javascript to load content and you're facing more advanced anti-scraping techniques. This mode uses a custom headless browser that can execute Javascript with advanced anti-blocking techniques. Some resources like stylesheets and images are not loaded for performance reasons. |

### Request Structure

```json
{
  "url": "https://example.com",
  "method": "GET",
  "headers": [
    "Authorization: Bearer <token>"
  ],
  "data": "{ \"key\": \"value\" }"
}
```

| Parameter  | Type | Description  | Example   | Required    |
|------------|------|--------------|-----------|-------------|
| `url`      | string | The destination URL to scrape | `https://example.com` | Yes |
| `method`   | string | The HTTP method to use | `GET` or `POST` | No |
| `headers`  | array | HTTP headers to send to the destination URL | `["Authorization: Bearer <token>"]` | No |
| `data`     | string | The HTTP body to send to the destination URL. Commonly used for `POST` requests. | `{ \"key\": \"value\" }` | No |

### Response

```json
{
  "request_id": "123e4567-e89b-12d3-a456-426614174000",
  "status_code": 200,
  "headers": {
    "server": "nginx",
    "content-length": "123",
    "content-type": "text/html"
  },
  "content": "<html><body>Hello, world!</body></html>",
  "has_errors": false,
  "errors": []
}
```

### Error Response

```json
{
  "request_id": "123e4567-e89b-12d3-a456-426614174000",
  "status_code": 401,
  "headers": {},
  "content": "",
  "has_errors": true,
  "errors": ["The API key you provided is invalid. Please check your API key and try again."]
}
```
