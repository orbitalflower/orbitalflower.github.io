---
title: "How secure is Lastpass?"
category: opinion
tags: security
redirect_from:
- 20150725-how-secure-is-lastpass.html
description: 
license: CC BY
---

Erratasec [ran a brief
analysis](http://blog.erratasec.com/2015/06/should-i-panic-because-lasthash-was.html)
to measure how hard it is to brute-force a Lastpass password file. It turns out
it's quite hard, but only if you have a strong master password.

The article attempts to break a password of the same algorithm and strength used
by Lastpass (100,000 rounds PBKDF2). A standard desktop PC can only attempt
2,577 passwords per second, compared to around 1 billion for a weaker hash
algorithm.

Given a full week, an attacker with no special equipment beyond a standard PC
can make just over 2<sup>30</sup> password attempts on a stolen Lastpass file.
That's enough to break [weak
passwords](https://orbitalflower.github.io/20150412-how-strong-is-your-password.html#weak-passwords),
such as any single word followed by up to four digits.

However, even a rich attacker will find that adding more computing power has
diminishing returns. A high-end rig built for $5,000 and running for a full year
can only make something in the range of 2<sup>41</sup> attempts, and it would
take a multi-million dollar exascale supercomputer (technology which may exist
by 2020) for a full year to break 2<sup>50</sup>. At that price, it would be
considerably cheaper for an attacker to install a keylogger on your computer.

So for Lastpass, specifically, a moderately strong master password of [4 random
words](https://duckduckgo.com/?q=passphrase+4+words) should protect your
password file sufficiently well that a wealthy adversary would have to spend a
lot of time and money for only a 1% chance of breaking your password.

This supports the idea that weak passwords are never safe (and most people use
weak passwords!), because even a strong algorithm can be broken trivially for
a small number of attempts. Conversely, an extremely strong password can never
be brute-forced even on tomorrow's supercomputers; data is never invulnerable,
but the strength of your password is no longer the weakest link.
