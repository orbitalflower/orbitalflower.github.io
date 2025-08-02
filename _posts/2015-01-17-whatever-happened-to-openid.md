---
title: "Whatever happened to OpenID?"
category: comp
tags: openid
redirect_from:
- 20150117-whatever-happened-to-openid.html
description: 
license: CC BY
updated: 2025-08-01
---

Created in 2005, OpenID was hailed as the future of web login. Now,
ten years later, almost no sites accept the OpenID login protocol
and Google plans to shut down its OpenID 2.0 service later this year.
So what went wrong?
{: .lead}

In December 2010, online news network
[Gawker Media was hacked](http://lifehacker.com/5712785/faq-compromised-commenting-accounts-on-gawker-media), leading
to the leak of passwords for 1.4 million user accounts. Hacks like
these are disastrous for users, who often re-use the same password
on multiple sites.

Not all Gawker users were affected. Gawker offered social media login,
where users can authenticate via another account like Facebook or
Twitter. For those users, Gawker never handled the password directly
so there was nothing to leak.

## Why OpenID was a great idea

Social login traces its roots back to OpenID, a system created in 2005
by the founder of LiveJournal. The idea was this: Instead of trusting
every site with your password, you only use it to log into your
OpenID provider. When another website asks you to log in, they simply
confirm your identity with your OpenID provider.

OpenID solved a growing problem with the web: __avoiding passsword
re-use__. Jeff Atwood summed it up [shortly after the Gawker attack](https://blog.codinghorror.com/the-dirty-truth-about-web-passwords/):

> In other words, the more web sites you visit, the more networks you
> touch and trust with a username and password combination -- the
> greater the odds that at least one of those networks will be
> compromised exactly like Gawker was, and give up your credentials
> for the world to see. At that point, unless you picked a strong,
> unique password on every single site you've ever visited, the
> situation gets ugly.

The more sites you sign up to, the more likely it is that at least one
will be hacked. When this happens, your password is effectively
compromised, unless you used a completely different password at every
website. But remembering all those passwords is difficult, and when
something is difficult, people will take the easier option.

OpenID solves that problem. Instead of trying to force users to remember
more passwords, it allowed users to remember only one. Early
adopters were hopeful that OpenID would eventually replace password
login almost entirely.

## What went wrong

Even though major internet suppliers operated as OpenID providers
(including Google, Yahoo, MySpace, AOL, Steam and Facebook), most
did very little to advertise the service and most users were unaware
that they had an OpenID identity (and still are). As a result,
OpenID was mainly used by those few technically minded users who
already knew about the system.

Few website operators saw the benefit of OpenID login. Users seemed
quite content to hand over their e-mail address and password. Even
sites that accepted OpenID still had to implement password login for
users who weren't hip with the new system.

OpenID providers became eager to supply more value. Derivative
technologies like OAuth (Twitter) and Facebook Connect offered
site owners not just authentication, but personal user information
and the ability to post on the user's social feed. Providers like
Facebook could in turn receive valuable marketing information.

The new "social" login alternatives were a huge success. Despite
compromising the user's privacy, they offer better usability:
users are presented with two or three login buttons for major
providers, instead of an "enter your OpenID" form where most
users were unaware that they even _had_ an OpenID.

## So long, and thanks for all the auth

OpenID was a lightweight, elegant solution to the problem of password
re-use. Sadly, it never took off, and major OpenID providers like
Google and Facebook are now [closing their OpenID service](https://developers.google.com/+/api/auth-migration).

The popularity of social login like Facebook Connect is a victory for
password security, but not for privacy. Sites can request personal data
like a list of all the user's friends with their real names, something
that would have been unthinkable in 2005. Social auth grants access not
just to a user's identity, but to their account, and this is what OpenID
was initially created to protect against.

Mozilla's [Persona](https://www.persona.org) is a newer OpenID-like
system which works with any e-mail provider, even if they haven't
yet implemented the Persona service. Unfortunately, even fewer sites
support Persona now than OpenID, partly because it doesn't give them
access to all the free marketing data they can get from
Facebook Connect.

**Update** (August 2025): Persona shut down in 2016.
