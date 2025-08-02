---
title: "Social logins still being misused"
category: opinion
tags: security
redirect_from:
- 20160504-social-logins-still-being-misused.html
description: 
license: CC BY
---

[A tweet from The
Register](https://twitter.com/TheRegister/status/727917341158215680/photo/1)
shows a tech conference whose Twitter-based login excessively requests full
account access.

This is the core problem now with social login. As long as sites can request
more access than normal, they will request it, and some users will grant it.

The UI flow goes like this:

* User clicks "Log in with Twitter"
* The small print warns the user that the website they're logging into gains
  almost full control of their Twitter account
* Since the user had already decided to use Twitter auth by this point, they are
  likely to allow it anyway

Full account access is in the Twitter API for things like mobile apps, not
social login. User authentication just requires a unique user identifier (such
as an email address) and a way to prove the identity that user (password in the
cast of first-party login, or OAUTH for third-party login). Full account access
is excessive.

## Imagine if this became the norm

When Gawker was hacked in 2010, the leaked user database included password
hashes and OpenID tokens were leaked. Those OpenID users were safest, since the
tokens had no power except to link a user to an email account.

But if a database of Twitter accounts is leaked, the potential damage is
considerably greater. The attacker can read the users' direct messages with
other users who didn't opt in to this. He can also read the user's private
account and private accounts they follow.

You can't opt out of other users trading away your trust like this, and there's
no legitimate need for such broad access just to handle a social login.

But as long as this kind of high-value login exists, site developers won't want
to settle for lower-level OpenID type login, and we can't rely on users to know
the difference.
