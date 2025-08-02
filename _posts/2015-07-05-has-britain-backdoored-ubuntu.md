---
title: "Has Britain backdoored Ubuntu?"
category: opinion
tags: security
redirect_from:
- 20150705-has-britain-backdoored-ubuntu.html
description: 
license: CC BY
---

> I've heard about a lot of companies with operations in the UK who are forced
> to backdoor their services to continue to operate. Scary.
>
> --- Jacob Appelbaum, [on
> Twitter](https://twitter.com/ioerror/status/616885237407182848)

If Appelbaum is correct, several British companies have been compelled by the
government to provide a government backdoor into their systems without notifying
users.

To be fair, he cites no sources and the statement might merely describe GCHQ's
_Mastering the Internet_ system which installs black boxes at ISPs, which was
already known to the public in 2009.

But if any UK company can be forced to backdoor their system in secret, the
possibilities are worrying.

UK based __Canonical Ltd__ produces Ubuntu Linux, used as a server OS by 8.2% of
all websites and by over 40 million people as a desktop OS. Canonical could be
forced to hand over the signing keys for the Ubuntu system updates, ship Ubuntu
with harmful privacy defaults, or serve backdoored copies of the Ubuntu ISO to
named IP addresses. Ubuntu ISO downloads are currently served over insecure HTTP
even though the site's wiki has a valid SSL cert.

The __Raspberry Pi Foundation__ has sold over five million Raspberry Pi units,
making it the best selling British-made computer since the Amstrad PCW. The
Raspberry Pi's low price and small power consumption make it useful as a router,
home server, firewall and other security-critical tasks. Most Raspberry Pi units
are manufactured in the UK, even though it's cheaper to import the finished
product from China than to import the components.
