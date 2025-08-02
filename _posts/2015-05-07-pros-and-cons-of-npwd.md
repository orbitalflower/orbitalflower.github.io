---
title: "The pros and cons of npwd"
category: comp
tags: security
redirect_from:
- 20150507-pros-and-cons-of-npwd.html
description: 
license: CC BY
updated: 2025-08-01
---

On Tuesday, Cryptocat creator Nadim Kobeissi released
[npwd](https://github.com/kaepora/npwd), a simple password manager that
generates passwords from a master password without the need for a password
database. This approach solves several problems, but has a few disadvantages.

A typical user chooses passwords that are easy to remember but easy for an
attacker to guess, and uses the same password on all sites because that's also
easy to remember. Any technological solution to this problem has to accept this
use case and work around it.

Password managers are particularly useful here: the user need only remember the
master password to his or her password software, which in turn can generate and
remember a different strong password for every site.

The difference with npwd is that it algorithmically generates a strong password
derived from your original password and the name of the website. Since it's
deterministic, the same password and website name will always give the same
output, meaning you don't have to store a password file, and don't have to
worry about losing your password file.

It's not an entirely new idea: most websites store passwords hashed with a salt
in this manner, and some users have applied the same method to generate stronger
passwords. Even applying the relatively weak SHA1 is beneficial since it turns
any password into 40 hexadecimal characters, completely impractical to brute
force _unless_ whoever is cracking the password is specifically guessing SHA1.

Where npwd is stronger is that it uses _scrypt_, an algorithm specifically
designed to be slow to calculate even in optimal circumstances. An expensive
mining rig for scrypt-based Litecoin (an AMD R9 290X GPU) only calculates
between 0.72 million and 1 million hashes per second, while the same hardware
calculating MD5 hashes has been benchmarked at over _10 billion_ per second
per GPU (oclHashCat). Depending on the variables, npwd may in fact be even
slower to brute force than Litecoin.

But while it's much stronger than a normal password, npwd has the same
drawbacks that apply to any key derivation password system like this.

Since the salt is the name of the website, an attacker can pre-calculate hashes
for a given site, particularly for weak passwords. Once one password is
broken, the attacker now knows the base password and can generate all others.
It's essentially just very good obfuscation of what may be a weak master
password.

With a traditional password manager, the generated passwords are completely
random, meaning they cannot be calculated from the master password - the
attacker needs the user's password safe, or the generated passwords can be
practically unbreakable.

Anyone sufficiently tech savvy to install a Node.js program from Github is also
likely to have the technical skill to install something that generates stronger
passwords. The only advantage to npwd's approach is that you don't need to store
a password file at all.

However, that one advantage has benefits in some circumstances. You don't need
to sync your password safe between multiple devices. Your password safe can't
be intercepted in transit or copied from your computer. You can't be forced to
unlock your password safe at a border checkpoint. You don't have to reset all
your passwords if you lose your password safe to theft or data loss (although
you do if someone cracks one of your passwords).

In conclusion, npwd makes passwords stronger, but for most people it's much
better to use a full-featured password manager. A properly randomly generated
very long password is practically unbreakable with today's technology or even
tomorrow's, while even the best password-stretching algorithm is still limited
by the strength of the original password.

## Links

* [npwd](https://github.com/kaepora/npwd) (no longer available)

**Update** (August 2025): npwd is no longer available, but this article will be
left up for historic interest.
