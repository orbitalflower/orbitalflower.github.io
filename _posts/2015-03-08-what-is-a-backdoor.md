---
title: "A backdoor by any other name"
category: opinion
tags: security
redirect_from:
- 20150308-what-is-a-backdoor.html
description: 
license: CC BY
---

Tech news lately discusses two sides to a debate: the US government, who
intend to insert a backdoor into encryption systems used by their own
citizens, and everyone else, who say this is mathematically impossible
without weakening the system's security, and don't want to use a
backdoored system.

NSA director Mike Rogers' solution to this conflict?
[Just don't call it a backdoor](http://justsecurity.org/20304/transcript-nsa-director-mike-rogers-vs-yahoo-encryption-doors/):

> So "backdoor" is not the context I would use. When I hear the phrase
> "backdoor," I think, "well, this is kind of shady. Why would you want
> to go in the backdoor? It would be very public."

But to be clear, what the director is asking for is literally a backdoor.

## What is a backdoor?

The Jargon File defines a
[backdoor](http://www.catb.org/~esr/jargon/html/B/back-door.html) as:

> A hole in the security of a system deliberately left in place by designers
> or maintainers. ... Historically, back doors have often lurked in systems
> longer than anyone expected or planned, and a few have become widely known.

Any deliberately-introduced security weakness in a system is a backdoor,
even if used for good purpose like protecting lives, and even if you call
it something else.

FBI director James Comey also argued for legally backdoored encryption
by calling it a
"[front door](https://www.techdirt.com/articles/20141019/07115528878/everybody-knows-fbi-director-james-comey-is-wrong-about-encryption-even-fbi.shtml)", a term
he wasn't able to define because it doesn't exist:

> We aren't seeking a back-door approach. We want to use the front door, with
> clarity and transparency, and with clear guidance provided by law. ... I
> don't think I am smart enough to tell you what 'front door' means.

But if a back door is a secret or obscure way in, the front door is the
entrance the user normally takes; in most systems, this means entering the
password. Britain already has "front door" access: it's illegal to refuse
to hand encryption keys to the authorities when asked. This allows
authorities to bypass encryption without weakening it in advance. The US
would have trouble introducing such a law due to the fifth amendment.

You'll notice that the UK is [still calling for backdoored crypto](https://www.schneier.com/blog/archives/2015/01/david_camerons_.html),
even when they have "front door" access. The main advantage of a backdoor is
to enable secret mass surveillance by intercepting and decrypting everyone's
data at all times, something which Amnesty International describes as
[a violation of fundamental human rights](http://www.amnesty.org.uk/blogs/ether/five-reasons-care-about-mass-surveillance-edward-snowden-gchq-nsa-citizenfour).

## Why backdoors always weaken security

A backdoor, by definition, is a weak spot in security. Even if that weak spot
is kept extremely secret, it still weakens security; it cannot improve it.

And that's assuming perfect circumstances: the secret is never leaked,
never discovered by security researchers, never misused by rogue employees
and never used illegally by agencies with access. If anything goes wrong,
the backdoor now grants access to people who shouldn't have access.

It turns out, things go wrong [quite often](http://www.cnn.com/2010/OPINION/01/23/schneier.google.hacking/index.html). Some concrete examples:

1. A few years ago, [Chinese hackers accessed users' GMail accounts](http://www.cnn.com/2010/OPINION/01/23/schneier.google.hacking/index.html)
using a backdoor Google inserted for the FBI.
2. Using its backdoor access to phone and Internet data, the NSA [illegally spied on US citizens](http://www.nytimes.com/2009/04/16/us/16nsa.html).
Not only that, but several employees used the system to [spy on ex-girlfriends](http://arstechnica.com/tech-policy/2013/09/loveint-on-his-first-day-of-work-nsa-employee-spied-on-ex-girlfriend/) and share stolen photos.
3. An unknown agency wiretapped the prime minister of Greece and other
high-ranking government minister between 2004 and 2005, using a backdoor
inserted by Ericsson.
4. In March 2015 an attack called [FREAK](https://www.schneier.com/blog/archives/2015/03/freak_security_.html)
was discovered that can break security on 36% of the Internet's secure
websites by forcing a downgrade to weaker RSA-EXPORT encryption keys.
These insecure keys were deliberately mandated by US law in the 1990s
to weaken encryption just enough that the NSA could break it. By 2015,
computers have advanced enough that anyone can break such a key in seven
hours for the cost of $100.

Cryptography expert Bruce Schneier explains it well:

> This is the generic problem with government-mandated back doors, key-escrow,
> "golden keys," or whatever you want to call them. We don't know how to
> design a third-party access system that checks for morality; once we build
> in such access, we then have to ensure that only the good guys can do it.
> And we can't. Or, to quote The Economist: "...mathematics applies to just
> and unjust alike; a flaw that can be exploited by Western governments is
> vulnerable to anyone who finds it."

Building a backdoor into a secure system is to give it an Achilles' heel.
