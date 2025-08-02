---
title: "Why I'm happy HTTP is going away"
category: opinion
tags: security
redirect_from:
- 20150514-why-im-happy-http-is-going-away.html
description: 
license: CC BY
---

Mozilla recently joined Google in plans to [all but ditch plain
HTTP](http://motherboard.vice.com/read/the-web-is-deprecating-http-and-its-going-to-be-okay):
Firefox intends to deprecate non-HTTPS connections, while Chrome plans to mark
non-HTTPS connections as insecure. Plain `http://` URLs seem to be going the way
of the dinosaur.

I'm okay with this.

A lot of people are seeing this as a compromise of freedom for security. In the
early days of the Internet, anybody could learn HTML buy a web domain, rent some
webspace and run a website of their own. Such sites are rare now: unfashionable,
obscure, abandoned and expired. But you still could, if you wanted.

If HTTP is phased out in favour of HTTPS, nobody will be able to run a website
of their own without investing in a secure certificate. The HTTPS infrastructure
favours the current ecosystem where end users host their content on major
centralised HTTPS-enabled platforms like Twitter, Youtube and so on.

But as I see it, the push toward HTTPS hinders personal webpages very little.

HTTPS is no longer expensive or difficult to set up. There are [free or cheap
SSL providers](https://konklone.com/post/switch-to-https-now-for-free). The
computing power required to enable HTTPS is negligible with modern hardware,
especially for a small website, and small sites typically don't have big-site
obstacles like legacy infrastructure or the current issue where advertising
networks haven't fully adapted to HTTPS sites yet.

Small website owners have always need a domain name (I can't remember the last
time I saw a website that ran on a bare IP address), so it's quite
straightforward to buy and renew a site's SSL certs at the same time.

The security benefits of HTTPS far outweigh the inconvenience. The threats are
very real. Nowadays, your data can be [routed through foreign
countries](http://arstechnica.com/security/2015/03/mysterious-snafu-hijacks-uk-nukes-makers-traffic-through-ukraine/),
intercepted by [any number of malicious
actors](https://twitter.com/FiloSottile/status/598848725830742016), or recorded
and searched by [rogue nations with long histories of human rights
abuses](https://orbitalflower.github.io/20150331-tory-policy-will-end-security-privacy.html).

HTTPS offers three extremely important protections here:

1. It authenticates the site, guaranteeing you're getting the real site and not
an impostor. An impostor could fraudulently obtain your passwords or personal
information, or send malware or viruses.
2. It prevents an attacker from monitoring the content of the session, something
which was used in Iran to identify gay Instagram users until that site enabled
HTTPS.
3. It prevents an attacker from _modifying_ the data, which could censor news
sites, insert propaganda or even inject viruses and malware into otherwise
trustworthy sites. Both the US and China already have such a capability, but
even small actors like free wifi operators have used this technique to inject
advertising into webpages.

Put another way, suppose you visit Google with HTTPS. Unless someone has
compromised Google---[which they have](https://en.wikipedia.org/wiki/MUSCULAR),
so perhaps this was a bad example...

Suppose you visit Wikipedia _without_ `https://`. You could be misdirected to a
fake Wikipedia, or the real Wikipedia with a virus injected into the page. Your
activity could be logged by the wi-fi operator, another user on your network, a
hacked device on your network, a hacked router, your employer, your ISP, your
government, a foreign government, Wikipedia's government, Wikipedia's hosting
provider, or anyone who operates Internet nodes between you and Wikipedia. If
you're in Iran or Russia and reading up on gay rights, for example, you could
end up in serious trouble, and even in freedom-loving countries people have a
right to defend their privacy.

These threats weren't quite so endemic in the early days of the Web, nor was the
danger well understood. Considering the benefits of a certificate, the minor
cost and inconvenience is certainly worth it.
