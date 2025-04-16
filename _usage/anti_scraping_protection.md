---
layout: page
title: Anti-Scraping Protection
nav_order: 4
---

# Anti-Scraping Protection

Scrapezoid has built-in anti-scraping protection to prevent you from being 
blocked by websites. This is done utilising a combination of techniques 
including:

- TLS fingerprint mimicry
- User-Agent spoofing
- IP rotation
- Residential IP rotation
- Captcha solving
- Custom patches when using browser emulation on Javascript endpoints

We aim to provide the most effective anti-scraping protection available 
and to give you a valid response for the first request that you make.

When Scrapezoid needs to deal with some anti-scraping technologies, it may
make more than one request to the destination URL. Scrapezoid will
attempt to detect various anti-scraping techniques and apply the appropriate
behaviour to get a valid response. This capability is available out of the box
and is fully integrated within Scrapezoid.

This might mean that a request will take longer to complete than usual. It's
recommended to use a generous timeout when the websites you're targeting are
using extensive anti-scraping protections.

## What if I get blocked?

If you get blocked by a website, we recommend retrying the request or attempting
the request via the `super-stealth` endpoint. Some websites that utilise
extremely advanced anti-scraping techniques may be beyond Scrapezoid's ability,
but our team will always do our best to help you out.


