---
title: "The problem with PGP, part 4"
category: opinion
tags: pgp
redirect_from:
- 20150716-the-problem-with-pgp-part-4.html
description: 
license: CC BY
---

Recently, a tutorial titled [Mutt, Gmail and
GPG](https://gist.github.com/bnagy/8914f712f689cc01c267) advised users to take
radically different steps to most other guides, including the standard GPG
documentation.

When two guides offer completely opposite advice and there's no general
consensus on which is right, it's a big problem. PGP is complex and most users
aren't able to make sufficiently informed choices about the secure way to use
it.

Some of the guide's advice deserves criticism:

* It recommends Gmail as an inconspicuous e-mail provider with good security
practices. However, using Gmail with IMAP requires either disabling two-factor
auth or bypassing it by generating an app-specific password (sixteen chars
lowercase, approximately 75 bits entropy). Gmail is usually unpopular with
privacy advocates as Google is a known NSA partner.
* The guide uses Mutt, a command-line mail client for which the guide admits the
default SSL settings are insecure. Mutt also stores passwords in plaintext. In
both cases the guide offers better settings, but it's not very reassuring to
know that your mail client isn't as secure as possible by default.
* It recommends disabling support for the system SSL certificate store and
manually validating certificates instead, despite [known opportunities for human
error](https://orbitalflower.github.io/20150219-why-pgp-will-never-be-mainstream.html):
since validating correctly is difficult and unnecessary to proceed, it's easy
for a user to accept invalid certs. Since Google certs renew every three months,
the user can become accustomed to accepting new certs.
* The guide recommends to never PGP sign messages, in order to have plausible
deniability. It's unreasonably optimistic to assume this would hold up in court.
Courtrooms routinely accept the validity of messages that aren't
cryptographically signed, and there will already be a copy of the message in
your Gmail outbox. Refusing to sign just makes it extremely easy for an attacker
to impersonate you, which the guide admits is a risk.
* It recommends against using keyservers. Since the guide also recommends
against signing messages, you now have no practical way to revoke or issue new
keys. The correct management of public keys in PGP is [already difficult and
controversial](https://orbitalflower.github.io/20150509-the-problem-with-pgp-part-2.html).

This is a general problem with PGP: guides on its use radically disagree, and
even the official documentation isn't completely authoritative on basic aspects
of its use.

But further, even the software that supports it, such as Mutt, is likewise
difficult to use and takes work to configure into something with strong
security. Comms software needs straightforward usability if it is to be popular,
and needs to be popular in order to be useful.

## See also

* [The problem with PGP, part 3](https://orbitalflower.github.io/20150516-the-problem-with-pgp-part-3.html)
* [The problem with PGP, part 2](https://orbitalflower.github.io/20150509-the-problem-with-pgp-part-2.html)
* [Why PGP will never be mainstream](https://orbitalflower.github.io/20150219-why-pgp-will-never-be-mainstream.html)
