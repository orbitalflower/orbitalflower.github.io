---
title: "Yes, the IP Bill has a backdoor clause"
category: opinion
tags: security
redirect_from:
- 20151106-yes-ip-bill-has-backdoor-clause.html
description: 
license: CC BY
---

Closer analysis of the Draft IP Bill shows that the UK government can still use
it to force companies like Apple to backdoor their encryption.

## Backdoor requirements

The Secretary of State can serve two kinds of notice: a technical capability
notice, for anything that requires a warrant under this act, and a national
security notice, for anything else.

### Technical capability notice

Section 189, "Maintainence of technical capability", allows the Secretary of
State to impose obligations on a relevant operator, defined as anyone who
provides telecommunications services or public postal services. These
obligations are extremely broad, and include:

* To "provide facilities or services of a specified description". Any operator
can be forced to provide literally any service, if it's within their technical
capability to do so.
* To remove "electronic protection" (which would includes encryption) applied by
a relevant operator. This includes _any_ such operator, meaning a company can
be forced to strip encryption employed by another company if it's within their
technical ability.

These obligations can be applied to people, companies or equipment outside the
UK, if the UK has a legal way to serve a notice. This might occur via mutual
assistance treaties, or by serving a notice to an international company's UK
headquarters.

Only three limits apply to a technical capability notice:

* It must be in pursuit of a warrant or notice issued under Part 2
(interception of communications), Part 3 (metadata collection without a
warrant), Part 5 (hacking) or 6 (bulk interception).
* The Secretary of State must considered the steps taken to be necessary to
fulfil the warrant.
* The Secretary of State must consider it reasonable that it is practicable for
the operator to comply.

### National security notice

Section 188 allows the Secretary of State to give a "national security notice"
to any telecommunications operator in the UK, requiring them to take any steps.

It specifically requires them to enable the intelligence services to do anything
the warrant says.

The limits:

* The Secretary of State must consider it necessary in the interests of national
security.
* The Secretary of State must consider the steps proportionate to the desired
goal.
* It may not require anything that a warrant is required for under the bill.
* It only applies to UK operators.

## Who does it apply to?

The bill plays a tricky game of definitions here.

### Telecommunications operator

National security notices apply to this kind of entity.

Section 193 defines a telecommunications operator as anyone who offers a
"telecommunications service" to someone in the UK, or provides a
"telecommunications system" which is wholly or partly in the UK or controlled
from the UK.

### Telecommunications service

Anyone who provides this kind of service can be subject to technical capability
notice.

Section 193 defines a "telecommunications service" as "any service that consists
in the provision of access to, and of facilities for the making use of, any
telecommunication system".

Access and/or making use of are further defined as facilitating the creation,
management, or storage of communications which may be transmitted.

### Telecommunication system

Section 193 defines a "telecommunication system" as any system anywhere in the
world that exists "for the purpose of facilitating the transmission of
communications by any means involving the use of electrical or electromagnetic
energy".

This is particularly vague, and the explanatory notes do not provide any
additional clarification. __This is where the loophole exists.__

A network engineer might argue that this only applies to the physical layer
(e.g. cables). But since data sent over the Internet ultimately travels over the
physical layer, a lawyer could argue that any company, including app developers,
fall under this category.

GCHQ interprets existing law as broadly as possible, and in secret. It will
absolutely take advantage of this situation.

## Does the UK install backdoors already?

Yes.

The introduction to the draft IP bill promises that the bill "will not impose
any additional requirements in relation to encryption over and above the
existing obligations in RIPA".

## What systems will be unaffected?

PGP, OTR, and other strong user-deployed encryption will be largely unaffected.
ISPs cannot be compelled to break encryption they have no ability to, nor does
the bill force them to forbid that encryption.

However, even these are not invulnerable. Intelligence and law enforcement have
explicit powers to hack devices, which will circumvent just about any
encryption.
