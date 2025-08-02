---
title: "An idea for secure e-mail"
category: opinion
tags: security
redirect_from:
- 20150827-an-idea-for-secure-email.html
description: 
license: CC BY
---

This is a naive idea for a way to make e-mail more secure.

## Problem

E-mail is ubiquitous, but not secure. The decentralised model makes it easy to
forge a sender's e-mail address, giving users no guarantee that their e-mail is
secure. It's radically easy for an attacker to send a user a link to an infected
website or an attachment in a vulnerable document format like .doc or .pdf,
which is common in business.

## Solution

### 1. Browsers manage user keypairs

* All web browsers should include a function to manage a PGP public key. If the
user does not have a key pair, the browser lets them generate one. It should be
4096 bits by default. It should include the user's e-mail address.
* A new standard should allow a website to request the user's public key from
the web browser. A popup in the browser asks the user to either select one of
his public keys or create a new one, or refuse the request. For maximum
compatibility, this standard should be compatible with existing HTTP standard,
such as using HTTP headers to identify that the site supports keys and giving
the URL that the browser can upload the key to; the user can also upload the key
manually via an upload form, though this is not encouraged due to the risk of
novice users accidentally uploading private keys or failing to understand the
complexity and abandoning the secure system altogether in favour of less secure
password login. HTTPS should be mandatory for this protocol in order to prevent
hijackers replacing the public key in transmission.
* The private key is never transmitted or held by anyone. Users will be
encouraged to store their key on a "login key", a Yubikey-style device which
stores their private key. These should become ubiquitous and compatible with
mobile devices via NFC or similar technology.

### 2. E-mail services run PGP keyservers

* All major e-mail providers should run PGP keyservers. These should use TLS.
* A web browser or operating system will, by default, sync keys with multiple
indepdendently run keyservers, ideally seven. At least half should use TLS. The
list of keyservers should be user-configurable to add user-preferred keyservers
or remove untrustworthy ones.
* When the user logs into a webmail service, their key is signed by the service.
For example, if Google is satisfied of a user's identity (login involving
two-factor) they will sign that user's public key with a key of their own, which
in turn may be signed by a securely stored Google long-term signing key similar
to the SSL signing framework. The user's signed public key will now authenticate
them to other sites as the Google user they claim to be.
* Governments may be able to compel a provider to sign a false key in order to
grant access to services or impersonate a user. Users can protect themselves
against this threat by removing untrusted keyservers from their trust list (e.g.
a US company may not trust a Chinese keyserver, or a UK company may not trust a
UK keyserver).

### 3. Webmail supports PGP

* All major webmail providers will be PGP-aware.
* Mail providers will __strip all HTML and attachments__ from messages which are
not signed. The user may be allowed to force the site to show the insecure
message, but should be strongly warned against it. Unsigned HTML e-mail should
be effectively deprecated.
* By default, mail should be signed, but encryption is optional. It may be
impractical for a mailshot to collect PGP keys for thousands or millions of
customers, and unnecessary when the content of the message is widely known to
the public anyway. However, signing is necessary so that, for example, Gmail can
assure the user that a message from Linkedin is genuine and the links are safe
to click.
* If the user has supplied a public key, their messages are automatically signed
unless this functionality is disabled overall (not recommended) or on a per-post
basis.
* When a user adds another to their contact list, they store each other's public
keys in their account, and, optionally, may export and download these keys
(perhaps assisted by functionality in the web browser or a plugin). Messages
from this user are marked as verified, e.g. by a green tick by the user's name.
Ideally, public keys should be pinned, and users notified when a key changes.
The user should be able to mouseover the green tick icon to see a tooltip
describing which authority signed the key.
* The user cannot be relied on to manually "sign" messages. Nor can the
currently standard verb "sign" be used to describe cryptographic signing, since
it is likely to be confused with the standard e-mail "signature" which appears
at the bottom of a message.
* Encryption should be available in the optional context of "secure e-mail" or
"private e-mail". In order for this feature to be meaningful it needs to have
the following assurances:
  * Where two users share secure keys signed by their e-mail provider, they are
  automatically offered the option of message encryption
  * Web browsers must support a secure textarea element which cannot be read by
  the site's Javascript
  * Client functionality removes the "secure" flag from the textarea only after
  the client has encrypted it, so that the plaintext is never transmitted to the
  webmail server
  * Users must be able to decide whether they want their decrypted e-mail to be
  re-uploaded to the site's store. E-mail uploaded in this manner becomes
  usefully searchable and can be read later even if keys are lost, but is
  vulnerable to warrantless disclosure under some countries' privacy laws (e.g.
  third party doctrine in the US)
  * Webmail should not support encrypted e-mail from unknown senders, to prevent
  spam effectively bypassing filters
  * The client should only offer a guarantee of security if the device is able
  to source sufficient entropy for required randomness in key generation

### 4. Public key also used for login

* The website can use the public key in a handshake to authenticate the user, as
a replacement for password authentication.

### 5. Key backup and revocation

* The user can backup their key to a Yubikey style device. Such devices can be
used to sign and encrypt but do not allow the private key to be read from the
device.
* Should all computers containing the original key be lost, the user can
generate a new key and sign it with the Yubikey style device. The provider will
accept it the replacement key if the e-mail address is the same.
* Should the physical login key token be lost, and the user has no other copies
of the key, the user can, if they still have account access somehow, revoke
their key and upload a new one at any time.
