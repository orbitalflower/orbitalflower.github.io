---
title: "Facebook now supports PGP"
category: opinion
tags: pgp
redirect_from:
- 20150602-facebook-pgp.html
description: 
license: CC BY
---

Facebook now allows users to upload a PGP public key to be used to encrypt
e-mails sent by the site.
{:.lead}

For such a major website to roll out support for PGP is a big step toward its
acceptance as a mainstream standard practice. Facebook's core business model is
handling massive amounts of private data and metadata and the e-mail
notifications it sends can leak significant information if unencrypted.

The browser extension [Mailvelope](https://github.com/mailvelope/mailvelope)
applies the metaphor that unencrypted e-mail is like a postcard without an
envelope, such that anyone can [read or modify it in
transit](https://orbitalflower.github.io/20150331-tory-policy-will-end-security-privacy.html).
It's an increasingly common attitude that encrypting mail must be made as
commonplace as sending letters in envelopes, and right now PGP is the closest
thing we have to an end-to-end e-mail encryption standard.

If Facebook also cryptographically _signs_ its e-mail, it will finally be
possible for users to verify mails from Facebook, making Facebook links safe to
click again.

## Drawbacks

However, the system isn't perfect.

Password resets will be encrypted. This means if you lose your password manager
and PGP key at the same time (e.g. your laptop is stolen), you won't be able to
reset the password to your account. This is a general problem in use cases like
Mailvelope where encrypted messages are kept on a server and loss of a key
renders them permanently unreadable. Many users do not have good backups, let
alone key backups, and cloud storage backups are a potential weak place to trust
with a private key.

Many security guides advise users to have their PGP keys expire after a period
of time, generally a few years. This means not only uploading new public keys
to Facebook every few years when you renew or replace keys, but doing the same
on every site that uses the same feature.

Facebook mails will be safe if signed, but phishing e-mails can still send
unencrypted mails, which are up to the individual mail client to identify as
insecure. Phishing may also send messages encrypted with the user's public key,
acquired from a public keyserver, and the user may regard the encrypted mail
with a false sense of authenticity. It's thus currently limited as a useful way
to prove authenticity.

Increased use of PGP will make it harder for server-side webmail features like
search and spam detection. This can be a problem since the user's e-mail client
will be responsible for its own spam detection, which isn't always practical on
a mobile device.

Governments still have access to your personal data since Facebook is a PRISM
partner; the exact level of access available is classified and subject to
change over time due to technical and legal issues, but the general idea is that
Facebook PGP mail does not protect your data from government surveillance
dragnets. It does protect you against most lesser threats, however.

Governments can now tie PGP keys to Facebook accounts, and thus to real-world
identities. The same technique has been used to link real-world identities to
web usage, IP addresses and other identifiers. Facebook users probably have
their real identity linked to their e-mail address, which in turn can be queried
from a PGP keyserver. This simply provides a stronger match and cuts out the
middleman.

## A positive step

Facebook's support for PGP is a welcome feature. E-mail is very much in need of
some kind of end-point encryption like HTTPS does for the web, and PGP is the
closest thing right now to an existing standard. As long as are to continue
using the old insecure e-mail system rather than abandon it for some new
secure-by-design messaging standard, the only practical solution is retrofit it
with what we've got right now, and what we've got is PGP.

## See also

* [The problem with PGP, part 3](https://orbitalflower.github.io/20150516-the-problem-with-pgp-part-3.html)

