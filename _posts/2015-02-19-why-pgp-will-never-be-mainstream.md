---
title: "Why PGP will never be mainstream"
category: opinion
tags: pgp
redirect_from:
- 20150219-why-pgp-will-never-be-mainstream.html
description: 
license: CC BY
---

Despite its strong reputation for security, PGP is unlikely to reach
mainstream popularity.
Not just because it's hard to use, but because it's easy to use wrongly.
{: .lead}

Last year, [@bcrypt](https://twitter.com/bcrypt) criticized PGP's design
for [relying on user actions](http://zyan.scripts.mit.edu/blog/certificate-transparency-for-pgp/):

> IMO, if we're trying to improve email security for as many people as
> possible, the best solution minimizes the extent to which the authenticity
> of a conversation depends on user actions. Key management should be invisible
> to the average user, but it should still be auditable by paranoid folks.

Any activity the user has to perform manually to ensure security introduces
security risks:

1. The user may find the steps too complicated or inconvenient and avoid them:
   1. If the system allows the user to opt out of security for the sake of
   convenience, they may do so
   2. If the system forces the user to take steps, they may refuse to use
   the system altogether
2. The user may perform the steps wrongly:
   1. If the system allows mistakes, the user now has the illusion of
   security
   2. If the system blocks on mistakes, it becomes harder to use

A great deal of encryption can be taken away from user action, and several
systems which do this have seen great success. The best known example is
probably HTTPS. It "just works": no special software to install or user
input required.

PGP's interface can be simplified, but never to the extent that it
"just works". Unlike HTTPS which uses a centralized authority system to
determine on the user's behalf, PGP uses a decentralized web of trust
and requires uses to work out for themselves whether their keys are
valid. Users are expected to manually curate a contact list by authenticating
each other over other secure channels or via mutual friends who also use PGP.
You have to work out for yourself whether the user is who they say they are,
and giving that responsibility to a human being opens up avenues of failure
while making the software inherently harder to use correctly.

As Yan points out, a communications system ultimately needs some way for
the user to be sure that the encryption key belongs to the user, and to do
this invisibly typically requires some central authority. While the authority
could pass out bad keys if compromised, it also protects the user from
accepting bad keys from another source.

PGP's other flaw is that it's not a communications protocol, but rather an
encryption system to be used with other communications protocols. Any system
using PGP must also support unencrypted communications, allowing users to
communicate freely even if they've forgotten to apply encryption. The
system fails to protect the user if they or their conversation partner
forget to lock up, which is easily done.

While PGP is a good encryption protocol, it's problematic as a user
communications protocol because key handling is too much effort for most
users and it's too easy to mess up at the cost of security. Most users
will stick with systems that implement encryption invisibly and use
centralized key authorities, such as HTTPS, WhatsApp and iMessage.
