---
title: "DuckDuckGo: Finding things without Google"
category: comp
tags: google
description: "An overview of some neat features of DuckDuckGo."
license: CC BY
last_modified_at: 
---

The [enshittification](https://en.wikipedia.org/wiki/Enshittification) of Google
continues with its pivot from search results to AI-generated answers.
[DuckDuckGo](https://duckduckgo.com/) originated in 2008 as a niche Google
clone with a few additional tools, but its killer feature is now that it _still
has search results_.

Aside from search results, there are a few additional features, mostly available
directly from the search bar. This article highlights some of the more useful
features.

## Search other sites

[Bangs](https://duckduckgo.com/bangs) are keywords preceded with a `!` symbol
which direct the search terms to another website, allowing you to search one of
several thousand sites directly.

For example, searching DuckDuckGo for `!w star trek` will search Wikipedia for
"star trek", in practice taking you directly to the Wikipedia page. `!wt` will
take you to Wiktionary, `!wq` to Wikiquote, and so on. `!startrek` will direct
your search to Memory Alpha, the Star Trek wiki.

Some other useful bangs include `!omap` for Open Street Maps, `!wbm` to search
the Wayback Machine for a given URL, `!py` for the Python documentation, and
`!php` for the PHP documentation.

You can use bangs to modify the DuckDuckGo search settings for one search, such
as `!safe` and `!safeoff` to enable or disable Safe Search, or `!i` to use image
search.  You can also search other search engines, such as `!g` for Google.

## Unit conversion

Conversion between units can be done directly. For example, searching DuckDuckGo
for `6 feet in cm` gives unit conversion, and currency conversion can be done as
easily, e.g. `100 JPY in USD`.

For more advanced conversions, use the `!wa` bang to directly search Wolfram
Alpha. You can do something like `!wa the circumference of the earth divided by
the speed of light`. See the
[Wolfram Alpha tour](https://www.wolframalpha.com/tour)
for examples of the calculations that site is capable of, including astronomy,
advanced mathematics, weather, and nutrition. For the calculations it has been
programmed with, Wolfram Alpha is more reliable than AI.

## Random number generation

You can roll dice using the keyword "roll" with D&D-style dice notation, such as
`roll 1d4`, `roll 10d6`, or `roll 1d20+4`. You will receive the results and a
total. It appears to support up to ten dice.

You can also type something like `random number between 1 and 20`.

It can also be used for password generation, using such phrases as `password`,
`password 32 characters`, or `passphrase 10 words`. If you're paranoid about
getting your passwords from a search engine, however, you might deploy a
[local script](https://github.com/orbitalflower/nyanpass).

## AI (or no AI)

Even DuckDuckGo has gotten in on the AI chatbot trend. <https://duck.ai> offers
free anonymous usage of various AI models, including an image generation feature
(with built-in safety filter, naturally).

If you want to ensure no AI at all, searching via <https://noai.duckduckgo.com/>
will do that. It attempts to detect and disable AI-generated images in Image
results, disables the Search Assist feature, and hides links to duck.ai. You can
also simply disable all three in settings.
