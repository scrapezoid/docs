---
layout: page
title: API Specification
nav_order: 2
---

# API Specification

## POST /api/v1/scrape

### Request

```json
{
  "method": "GET",
  "url": "https://example.com",
}
```

### Response

```json
{
  "status": "success",
  "data": {
    "html": "<html><body>Hello, world!</body></html>"
  }
}
```

## POST /api/v1/scrape/js

```json
{
  "method": "GET",
  "url": "https://example.com",
}
```

## POST /api/v1/scrape/js/super-stealth

```json
{
  "method": "GET",
  "url": "https://example.com",
}
```


