---
title: "When can you use a weak password?"
category: opinion
tags: pgp
redirect_from:
- 20150517-when-can-you-use-weak-password.html
description: 
license: CC BY
---

It's possible to objectively [measure the strength of a
password](https://orbitalflower.github.io/20150412-how-strong-is-your-password.html)
against brute-force attack, but since strong passwords also tend to be difficult
to remember it's worth considering the situations in which a weaker, easier
password would be sufficient.

## Risk level

There are roughly three situations in which an attacker tries to obtain access
to your account or system:

* __Indirect access__ (Low): The attacker hasn't compromised the security of the
website or device he's trying to log into, and is limited to making a few login
attempts per minute.
* __Direct access__ (High): The attacker has breached security and obtained an
encrypted file, device or hashed password list. They can now attempt a brute
force attack at their own leisure, potentially millions or billions of password
guesses per second.
* __Immediate access__ (Very high): The attacker has directly obtained the
account password or unencrypted data, perhaps by fraud, hacking, physical theft
of a device or lawful warrant in their country. Password strength is now
irrelevant.

## Situation 1: Indirect access

In this situation, someone attempts to log in to your online account, but due to
technical limitations and the provider's security precautions they can only
guess a relatively small number of passwords per minute.

Ideally, you should only have to remember the password to your main e-mail
account, which should be at a reliable provider like Yahoo or GMail. All other
passwords can be stored in your password manager or web browser, since you can
reset account passwords as long as you can access your e-mail. Most accounts,
then, can have randomly-generated strong passwords that you don't need to worry
about.

A major e-mail provider is likely to limit the number of attempts an attacker
can make per second. Google, for example, starts showing CAPTCHAs which prevents
automated software from logging in at a high rate. Even websites without this
security measure, it's probably not feasible for an attacker to make as many as
a million login attempts per second. One attempt per second is more plausible.

An attacker making one attempt per second could guess every commonly-used
English word (about 100,000 possibilities) within a day. Within a year they can
make around 2<sup>24.9</sup> attempts, enough to guess every common word
followed by two digits and nearly every combination of two common words.
[Weak
passwords](https://orbitalflower.github.io/20150412-how-strong-is-your-password.html#weak-passwords)
are clearly insufficient even on a secure site.

If able to make 1,000 logins per second, even after ten years the attacker could
make only around 2<sup>38</sup> password guesses, which is just under a 1%
chance of guessing a password from a search field of 2<sup>45</sup> guesses. A
[moderate
password](https://orbitalflower.github.io/20150412-how-strong-is-your-password.html#moderate-passwords)
is potentially under threat here, but a stronger one (e.g. xkcd-style four
common words) is outside of this range. This is very approximately the upper
bounds of what an attacker can do without gaining direct access to a system.

## Situation 2: Direct access

An attacker has physical access to some encrypted data or system: they're within
physical range of your Wi-Fi signal, have stolen your encrypted smartphone or
PC, copied an encrypted file from cloud storage or downloaded a website's hashed
password list.

They can now make brute force password attempts as fast as their hardware
allows, and for as long as [Moore's
Law](https://en.wikipedia.org/wiki/Moore%27s_Law) holds up, the power and
cost-effectiveness of brute force password cracking systems will increase
exponentially over time.

According to [records on Wikipedia](https://en.wikipedia.org/wiki/FLOPS), in
1997 a group of Beowulf clusters could be built with a top speed of around 25
gigaFLOPS for a million dollars in today's money. By 2007, a cluster capable of
the same could be built for a mere $1,265 - over 800 times more calculation per
dollar. By 2013, the same $1,265 could buy 11,265 gigaFLOPS.

In practical terms, [oclHashCat](https://hashcat.net/oclhashcat/) gives the
following benchmarks for a $5,000 system with eight AMD R9 290X graphics cards
capable of approximately 45 teraFLOPS:

| Encryption type  | one second    | one day        | one year       |
| ---------------- | -------------:| --------------:|---------------:|
| WPA/WPA2         |      1.536m   | 2<sup>37</sup> | 2<sup>45</sup> |
| Whirlpool        |   1122.304m   | 2<sup>46</sup> | 2<sup>54</sup> |
| MD5              |  92672m       | 2<sup>52</sup> | 2<sup>61</sup> |
| NTLM             | 175808m       | 2<sup>53</sup> | 2<sup>62</sup> |

Even with WPA2, a weak Wi-Fi password is broken within days. Passwords for
Whirlpool-based disk encryption are broken up to 8 characters full alphanumeric
within a week and 9 characters within a year. MD5, still used by many websites
to hash their passwords, breaks every 10-character alphanumeric and 13 character
alphabetic within a year, and in practice even more than this since passwords
[tend to follow predictable
patterns](https://orbitalflower.github.io/20150328-stop-numb3r1ng-up-passwords.html).

And attacks will only grow faster and more capable with time and money. A nation
state, large company or criminal group can use million dollar hardware and add
about __8 bits__. Each year, Moore's Law adds about __1 bit__, and spending a
year instead of a day adds about __8.5 bits__. There's also a 1.6% chance of
finding something that should be __6 bits__ above capability. And, on average,
something will be found halfway through the set, effectively squeezing out
another __1 bit__.

Strong passwords (75 bits and higher) are vital if an attacker can
make direct access to a system. Weak passwords are trivially broken, and
moderate passwords with sustained effort.

## Situation 3: Immediate access

An attacker has gained the password already through some means, or else has
acquired the unencrypted data or access to an unencrypted system. Either way,
the password strength is now completely irrelevant.

In this case, other protective measures are necessary. Encrypt data where
possible, and take steps to safeguard both the software of your device and its
physical security. If the attacker can gain physical access to unprotected data,
the password is irrelevant.

A corollary of this is that an attacker can steal a password from a site that
uses poor security, then go on to use that password successfully at a site where
password cracking isn't an option. Password re-use is therefore an extremely
poor idea (if you can only remember one password, use a password manager
software).

## Conclusion

* __Very weak passwords:__ Very weak passwords include single words
(even modified), personally identifiable information, very short passwords, or
any password even partly used elsewhere. __Never use these.__
* __Weak passwords:__ A password made of two common words or which is shorter
than 8 characters is generally weak. Don't use this for anything either.
* __Moderate passwords:__ Three or four random words. Suitable for __online
services__ with a good security track record, which don't allow continuous
login attempts, and __in conjunction with two-factor authentication__. However,
these are not secure enough to use as encryption keys or Wi-Fi passwords, and
can be broken with a little effort.
* __Strong passwords:__ Six random words, or 16 random alphanumeric characters.
These are in an unfortunate middle-ground: harder to remember than a moderate
password, but not as secure as very strong passwords. Right now they're as good
as very strong passwords, but in future they'll be as weak as moderate
passwords. Bear in mind that somone could simply hold on to leaked data for a
few decades and crack it later.
* __Very strong passwords:__ 10 common words, 22+ alphanumeric, or even 28+
lowercase is strong enough that security experts believe it impractical to crack
even with advanced computers 50 years from now. Nearly impossible for normal
humans to remember, but when __using a password manager__ to remember passwords,
there's no reason to use any weaker password unless the site has a maximum
password length.

## See also

* [How strong is your password?](https://orbitalflower.github.io/20150412-how-strong-is-your-password.html)
* [Stop numb3r1ng up passwords, and other advice](https://orbitalflower.github.io/20150328-stop-numb3r1ng-up-passwords.html)
