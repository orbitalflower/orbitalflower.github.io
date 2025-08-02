---
title: "Stop numb3r1ng up passwords, and other advice"
category: comp
tags: security
redirect_from:
- 20150328-stop-numb3r1ng-up-passwords.html
description: 
license: CC BY
---

Intel's [World Password Day](https://passwordday.org/en/) 2014 website is
a mess of distracting animated gifs, poor content flow and hit-or-miss
password advice.

## Numb3r1ng up passwords is weak

Swapping letters for numbers in your passwords is common advice, but the
security gains are minimal.

It assumes that attackers are still using a straight dictionary attack to guess
every word in the dictionary, so that "hunter" would be cracked but not
"hunt3r". In practice, password cracking software routinely checks such obvious
variants (e->3, o->0), well known to hackers since the 1980s
as [leet speak](https://en.wikipedia.org/wiki/Leet).

## Obvious punctuation is obvious

Joe's password is "hunter2". A website requires that passwords require symbols
and capital letters. Joe's password becomes "Hunter2!"

Requirements like these make two mistakes. They assume users will make more
than the minumum adjustment necessary, which often isn't the case. And again,
they seem to assume attackers are using straight dictionary attack, when
it's trivial to check for common variants.

## Phrases are good, but not perfect

The phrase "I am a hunter" is a much stronger password than "hunter", since
it's longer. However, English sentences are more predictable than random,
and an advanced attacker can use this to their advantage by eliminating guesses
that don't make sense in English. It would be better to choose four words at
random.

## Popular names are weak

Microsoft's advice for kids is to take a song or game title and swap some of
the characters. Great job, hackers will never guess
"[ruensc4pe](http://www.runescape.com/)".

The flaw with all these password schemes is that they start with a known
weak password, then increase its complexity in ways that give only perhaps
5% to 10% greater
[password entropy](https://en.wikipedia.org/wiki/Password_strength).

The result is a __false sense of security__.

## The key to strong passwords

A password is strong if it is both __long__ and __unpredictable__ (random).

This maximizes the number of possible guesses so that it is computationally
infeasble for an attacker to successfully find your password even by repeated
guessing.

The easiest and most effective way to do this is to __add random words to your
password__. Analysis of a property called password entropy shows that adding
a single randomly chosen word to your password is several times more effective
than any of the popular "tricks" like numb3r1ng, and often easier to remember.

## Password entropy

Suppose you lock a phone with a four digit pin code. Your pin has only 10^4
(ten to the power of four) or 10,000 possible values (from 0000 to 9999).

Now consider that a password cracking program might be able to guess
over a billion passwords per second, and it becomes clear that we need
something better than digits, and we need more than four of them.

Suppose we take a character set with 64 values: 26 lowercase, 26 uppercase,
10 digits and two symbols. We can represent 64 as 2^6, and say that each
such character has 6 bits of entropy. Each character, if it's chosen entirely
at random, adds 6 bits to our password.

For comparison, a common word (randomly chosen from top 10,000 used words) has
about 13.29 bits, and gimmicks like numb3r1ng only add one bit per character
at best. A low-end PC can break a 25-bit WPA password in _one hour_. A few
thousand dollars can break 40 bits WPA in two weeks or crack MD5 password
hashes at over 60 bits in a year. _Please leave the leetspeak to the 1990s
hacker bulletin boards_.

## Random-character vs random word

Base64 at 10 characters reaches 60 bits (breakable with sustained effort).
At 12 chars it has a strength of 72 bits (maybe large governments in ten years)
and at 16 has 96 bits (highly secure).

However, humans have difficulty remembering as many as sixteen completely
random things, which is disastrous for passwords. A solution is to use
a series of words instead of characters. You're essentially compensating
for the smaller password length by using a very large character set.

There are two popular approaches: XKCD style, and Diceware.

### XKCD style

This type of password appeared in [XKCD comic #936](https://xkcd.com/936/),
which noted a lot of the things mentioned above. The process is to pick
four words at complete random. The example given is "correct horse battery
staple".

The easiest way to do this is search DuckDuckGo for a phrase like
[passphrase 4 words](https://duckduckgo.com/?q=passphrase+4+words).
You'll be given a password chosen from
[a word list](https://github.com/duckduckgo/zeroclickinfo-goodies/blob/master/share/goodie/passphrase/words.txt).

The list currently stands at 4,293 words, giving 12.07 bits entropy per
word or 48 bits for four words. It's worth noting that the list was weakened
from 7776 words, which was equivalent to Diceware's strength of 12.92 bits
per word or 51.7 bits per four words.

You can find larger dictionaries, such as the top 10,000 words
(13.29 bits/word) or unixdict (around 16 bits per word). As of writing,
DDG will give you 60 bits for five words, 72 bits for six, and 96 for eight.

### Diceware

[Diceware](http://world.std.com/~reinhold/diceware.html) is a system where you
choose words from a list by rolling dice. Using real physical dice ensures
good randomness, since a computer could have a poor random number generator or
may even have been compromised.

Diceware uses a 7776 word list, equivalent to 6^5 since you roll five six-sided
dice to generate each word. The words are short for ease of typing, and you
can find variant lists for other languages.

Four words gets you 51.7 bits, five words 64.62 bits, six 77.55 bits, and
seven a respectable 90.47 bits.

## Other advice

1. Your password probable sucks and you suck at making passwords that are hard
for a computer to guess. Have a computer pick your password randomly, then
try to find a mnemonic.
2. You'll be surprised how well you remember complex passwords after typing
them often. Eventually it becomes muscle memory.
3. Write your complex password down until you've memorized it, then destroy
the paper or keep it in a secure, secret location.
4. Actually, avoid using passwords wherever you can. Use a password manager.
If you can't be bothered, [generate random passwords](https://duckduckgo.com/?q=password+30+strong)
for each site you sign up to and have your web browser remember it. Don't just
use the same password on multiple sites.
5. Don't rely on your password manager for your main e-mail account. You'll
need your e-mail to reset all your other accounts' passwords if you lose your
password manager.
6. Use 2-factor auth wherever you can, but especially your main e-mail account.
Keep backup codes in case you lose your phone or auth device.
7. Stop clicking links in e-mail.
8. Stop trusting public wifi, or wireless at all if it can be helped.
9. Technically, a tin foil hat is made from aluminium, not tin.

## See also

* [Intel #5habits](https://digitalsecurity.intel.com/5habits/)
