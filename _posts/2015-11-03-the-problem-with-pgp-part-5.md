---
title: "The problem with PGP, part 5"
category: opinion
tags: pgp
redirect_from:
- 20151103-the-problem-with-pgp-part-5.html
description: 
license: CC BY
---

GPG is adding support for Trust On First Use (TOFU), because Web of Trust is too
hard:

>  In contrast to the Web of Trust (WoT), TOFU's security guarantees are rather
>  weak. When using the WoT correctly, you can have high confidence that if
>  GnuPG says a given key is controlled by a specific user, then it probably is.
>  TOFU, on the other hand, is only able to detect when the key associated with
>  an email address has changed. Despite this, TOFU will be more secure than the
>  WoT for most users in practice. This is because using the WoT requires a lot
>  of manual support, __which most users never both with__.
>
> --- [GnuPG News, October 2015](https://gnupg.org/blog/20151103-gnupg-in-october.html)

Anything the user must learn to do manually is difficult and prone to error. PGP
relies on the user to manually operate the Web of Trust to validate keys, but in
practice this is so difficult that most people completely ignore it.

Web of Trust is only practical in tightly-knit communities, such as companies or
social groups. Validating a key requires that someone you already trust has
signed their key. If you want to communicate with someone more than one or two
degrees of separation away, you an unbroken chain of signatures to your
recipient. Often, because PGP is uncommon, there isn't even an unbroken chain of
PGP users to your recipient.

## Use case

Suppose you want to e-mail Edward Snowden, and grab his PGP key from a
keyserver. It might be signed by ten people, none of whom you know, so you can't
validate the key.

Suppose his key is signed by Glenn Greenwald, and you grab his key from a
keyserver. It's signed by twenty people, none of whom you know, so you still
can't validate Snowden's key. Maybe your friend trusts Greenwald's key, but she
never signed it or he never uploaded a version with her signature attached, so
PGP can't validate.

You can manually validate the key by checking the fingerprint Greenwald
publishes on Twitter, or downloading his key via The Intercept's website, both
of which use HTTPS and are generally considered reliable public sources that are
difficult to manipulate without someone noticing.

But this effectively only circumvents the trust issue by relying on a third
party secure channel, and that poses a question: why don't we just use that
secure channel to distribute our keys? It's still the default for keyservers not
to use TLS, leaving the user to rely entirely on a Web of Trust system that most
of your recipients don't bother to participate in.

## OpenPGP DANE

GnuPG recently implemented support for placing PGP keys in DNS records.

The [OpenPGP
DANE](https://datatracker.ietf.org/doc/draft-ietf-dane-openpgpkey/?include_text=1)
proposed standard admits that "keyservers are not well suited to support email
clients and MTA's to automatically encrypt email - especially in the absence of
an interactive user."

But it also warns that "this resource record is not a replacement for verifying
OpenPGP public keys via the web of trust signatures, or manually via a
fingerprint verification."

Since Google failed to include DANE support in Chrome, it's quite likely that
they will fail to support OpenPGP DANE for their users, leaving users reliant on
flawed keyservers.

## Is TOFU good?

Trust On First Use is kind of like key pinning: it won't validate the key, but
it will warn you if it changes. With PGP, this only happens if you add a new
key, in which case you knew about the change already, or refresh the keys from
the server and receive an update.

It's a somewhat defeatist measure that admits users don't bother to validate
their keys at all, and the best we hope to do is let them use untrusted keys to
avoid warning-blindness.

It's better than nothing, but doesn't solve PGP's big problem that manual key
verification is hard.

## Alternatives

I've [thrown about ideas
before](https://orbitalflower.github.io/20150827-an-idea-for-secure-email.html),
one or two of which may actually have any value.

Webmail providers like Google could sign keys uploaded by logged-in users. Most
people know and trust Google, whereas almost nobody (relatively speaking) knows
the two friends you got to manually sign your key. Anyone who doesn't want to
trust Google can additionally rely on old-fashioned Web of Trust.

Google can also publish public keys the same way Github does. A standard API
could be created which allows both humans and other e-mail services and clients
to retrieve public keys from the webmail provider over HTTPS using a simple URL
format and plain ASCII output.

Even so, PGP will not succeed until this is integrated into e-mail by default
just as SSL was integrated into web browsers, and is easy to use correctly just
as SSL was. That's a high standard, and it may well be that most users will
never progress past using whatever security measures their app or website allows
by default.

## See also

* [The problem with PGP, part 4](https://orbitalflower.github.io/20150716-the-problem-with-pgp-part-4.html)
