---
title: "Public keys must replace passwords"
category: opinion
tags: security
redirect_from:
- 20150706-public-keys-must-replace-passwords.html
description: 
license: CC BY
---

The use of passwords for web login is no longer sustainable. Humans cannot
easily remember multiple passwords or complex passwords, and the passwords we
generate tend to be highly predictable.
{:.lead}

The result is that weak passwords and password re-use on the web are extremely
common, with horrendous consequences for security.

Today, nobody knows this better than Italian hacker Christian Pozzi, whose
spyware company Hacking Team was itself hacked. In an uncanny vindication of
March's article [Stop numb3r1ng up passwords, and other
advice](https://orbitalflower.github.io/20150328-stop-numb3r1ng-up-passwords.html),
Pozzi's password was "Passw0rd", or for sites that required special characters,
"Passw0rd!81".

## Passwords aren't good enough

For a password to be secure it must be randomly generated and sufficiently long,
and a different password must be used on every site. Since it's difficult to
remember many complex passwords, and sites can't detect password re-use, the
failure mode is weak security.

One solution to that is to have a password manager generate and store strong
passwords, but that's not part of most user habits for the same reason most
people don't fit burglar alarms until after they've been burgled. To solve this,
storing passwords on the computer must be made the default.

But once we've offloaded password-remembering to the computer, we're no longer
bound by the limits of what humans can remember or type. There's no reason to
stick with the traditional password paradigm, aside from legacy support. We're
free to use a more advanced security technology: public keys.

## Public keys solve practical problems

Public keys solve the biggest problems that passwords currently face:

* Public keys are secure by default _even if leaked_, allowing key re-use
without compromising security. Unlike a password, an attacker who steals your
public key from one site cannot use it to impersonate you on another site.
* Since public keys must be computer-generated and cannot be chosen by a person
like a password, it's not possible to pick a weak key due to human bias.
* Phishing is useless, since an attacker cannot do anything with your public key
except identify other accounts which use that public key.
* The private key can be stored on a separate write-only hardware dongle so that
it cannot be stolen even if the computer is hacked. Even then, it can't be
keylogged.
* Unlike a password manager, it's not necessary to maintain a password file and
keep it synced between devices.

It even compares well to other alternative login technologies:

* __OpenID__: Relied on a third-party infrastructure, the largest providers of
which have shut down, locking some users out of their accounts. Public/private
key pairs held by the user don't have this problem.
* __Facebook login__: Typically shares private personal information with the
target site, and the site has a mechanism to ask users for other Facebook
account data or permissions that should not be granted. Reliant on Facebook
infrastructure, and Facebook could drop the feature later.
* __Mozilla Persona__: Has the same problems as OpenID and Facebook login, but
less beneficial to site owners since it doesn't let them request private user
marketing data like Facebook login. As a result, it's unlikely to gain traction.
* __Medium passwordless login__: A login link sent to your e-mail avoids the use
of passwords, but e-mail is no longer considered a secure system. It can be
unreliable or slow and a spam filter can eat your login mail.

## Why isn't it available yet?

Public key login is already a standard feature for systems like SSH, but not web
login. Unforunately, alternative login technology has always had [trouble getting off
the
ground](https://orbitalflower.github.io/20150117-whatever-happened-to-openid.html),
and any such system would need to be widely supported in all major browsers
before could supplant password login entirely.

FIDO UAF and U2F systems are perhaps the closest thing so far, but neither
standard seems to be trying to replace passwords just yet. U2F is only intended
to supplement passwords as a second factor, while UAF is more about supporting
biometric authentication on a site where the user already has a password.
Support is currently limited: U2F, originally developed by Google, is supported
by Google Chrome and the Google website, but very little else yet. And both
require extra physical hardware, which poses a barrier to entry.

Until there is strong support for public key auth, most users will be content to
number up their password and put exclamation marks at the end.
