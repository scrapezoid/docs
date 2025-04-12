---
layout: page
title: Getting Started
nav_order: 1
---

# Getting Started

It's easy to get started with Scrapezoid. By following the steps below, 
you'll be scraping the web in no time.

## Create an account within the Scrapezoid Console

To get started, you'll need to signup and create an account via 
the [Scrapezoid Console](https://console.scrapezoid.com/signup).

## Subscribe to a Scrapezoid plan

Once you have an account, you can subscribe to a Scrapezoid plan on the 
[Scrapezoid Plans](https://console.scrapezoid.com/plans) page.

## Get your API key

Once you have subscribed to Scrapezoid, you can find your API key in the 
[API Keys](https://console.scrapezoid.com/api-keys) page.

## Run your first scrape

Now that you have your API key, you can make your first API call to make
sure that everything is working. Here's an example using `curl`:

```bash
curl -X POST "https://api.scrapezoid.com/api/v1/scrape" \
     -H "X-Scrapezoid-Auth: YOUR_API_KEY" \
     -H "Content-Type: application/json" \
     -d '{"url": "https://example.com"}'
```





