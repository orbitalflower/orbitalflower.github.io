---
title: "The problem with PGP, part 2"
category: opinion
tags: pgp
redirect_from:
- 20150509-the-problem-with-pgp-part-2.html
description: 
license: CC BY
---

From the [GnuPG FAQ](https://www.gnupg.org/faq/gnupg-faq.html)

> __"Why do I need to validate certificates?"__
>
> A certificate can claim to be from anyone. You have to make sure that the
> certificate really belongs to whom it claims it belongs to.

> __"How do I validate certificates?"__
>
> This advice is controversial. It’s controversial for a simple reason: every
> Tom, Dick and Harry has their own idea about the “right way” to validate
> certificates. Some of these people are well-informed and some of them are just
> plain unhinged.

For PGP communication to be secure, the sender and recipients must manually
validate each other's keys, even though there is no general consensus on the
right way to do this.

The documentation suggests a complex process including meeting them in person
and checking two forms of government-issued ID, something which just isn't
always possible given the global nature of the Internet. It's generally easier
to ignore validation or send the message without PGP, so in a great many cases
that's what's going to happen.

Compare this to HTTPS, where all you need to do is insert an 's' after 'http'.

## See also

* [Why PGP will never be mainstream](https://orbitalflower.github.io/20150219-why-pgp-will-never-be-mainstream.html)
