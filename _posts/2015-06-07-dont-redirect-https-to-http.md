---
title: "Don't redirect HTTPS to HTTP"
category: opinion
tags: security
redirect_from:
- 20150607-dont-redirect-https-to-http.html
description: 
license: CC BY
updated: 2025-08-01
---

Some websites support HTTPS URLs, but then redirect to HTTP.

Don't do this. If you have HTTPS capability, just serve the page over HTTPS.

It's even worse than not supporting HTTPS at all, because you give a false sense
of security before dropping the user to HTTP.

**Update** (August 2025): I haven't seen any site do this in a long while.
Good job.
