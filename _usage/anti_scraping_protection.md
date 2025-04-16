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
- The use of residential IP addresses
- Captcha solving
- Custom patches when using browser emulation on Javascript endpoints

We aim to provide the most effective anti-scraping protection available 
and to give you a valid response for the first request that you make.

When Scrapezoid detects some anti-scraping technologies, it may result in
Scrapezoid making more than one request to the destination URL. This behaviour
is triggered automatically and is fully integrated within Scrapezoid.

This might mean that your API request may take longer to complete than usual. It's
recommended to use a generous timeout when the websites you're targeting are
using extensive anti-scraping protections.

## What if I get blocked?

If you get blocked by a website, we recommend retrying the request or attempting
the request via the `super-stealth` endpoint. Some websites that utilise
extremely advanced anti-scraping techniques may be beyond Scrapezoid's ability,
but our team will always do our best to help you out.


