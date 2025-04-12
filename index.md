---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Home
layout: home
---

# Scrapezoid

Scrapezoid is a web scraping API that gives you web scraping superpowers.

Scrapezoid was born due to some of the frustrations with other web scraping services.
Many claim to be able to work around anti-scraping measures, but in our experience,
very few actually work. Scrapezoid was built to be reliable and easy to use.

Many other services also have restrictive rate limits and request limits. It's
common that a lot of data is needed for many data science and machine learning
projects. We've designed Scrapezoid to able to scale for larger scraping projects.

## Features

### Flexible web scraping modes

Scrapezoid supports 3x different web scraping modes. Each mode has different
tradeoffs and is suited for different use cases.

1. **Fast mode:** scrape websites like a curl request, with basic anti-blocking.
It's recommended to use this mode for most use cases. If you find that
the website you're scraping is blocking your requests, or you require
Javascript so that the site loads correctly, you can try Javascript mode.
2. **Javascript mode:** scrape websites via a custom headless browser that can
execute Javascript with basic anti-blocking techniques.
3. **Super Stealth mode:** scrape websites via a custom headless browser that can
execute Javascript with advanced anti-blocking techniques.

## Why Scrapezoid?

Scraping web content at scale can be a pain. You often need to deal with
captchas, rate limiting, and other anti-scraping measures. It's a significant
amount of work to build a solution yourself. Some popular browser automation tools
can also introduce memory leaks and regular crashes.

Many services claim they work reliably and can deal with anti-scraping technology.
It turns out that most of them do not live up to these claims. Scrapezoid was 
originally built to actually provide a reliable web scraping service.

