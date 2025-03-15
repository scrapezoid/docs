---
layout: page
title: Getting Started
nav_order: 1
---

# Getting Started

It's easy to get started with Scrapezoid. By following the steps below, 
you'll be scraping the web in no time.

## Create an account on RapidAPI

To get started, you'll need to signup and create an account via 
RapidAPI. You can do that by going to [RapidAPI](https://rapidapi.com/)
and following the steps to create an account.

## Subscribe to Scrapezoid

Once you have an account, you can subscribe to Scrapezoid on RapidAPI. 
There is a free plan option you can use to get started. 
[Subscribe to Scrapezoid](https://rapidapi.com/scrapezoid/api/scrapezoid).

## Get your API key

Once you have subscribed to Scrapezoid, you can find your API key in the 
RapidAPI dashboard.

## Run your first scrape

Now that you have your API key, you can make your first API call to make
sure that everything is working. Here's an example using `curl`:

```bash
curl -X POST "https://scrapezoid.com/api/v1/scrape" \
     -H "X-RapidAPI-Key: YOUR_API_KEY" \
     -H "Content-Type: application/json" \
     -d '{"url": "https://example.com"}'
```





