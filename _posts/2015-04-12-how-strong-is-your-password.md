---
title: "How strong is your password?"
category: comp
tags: security
redirect_from:
- 20150412-how-strong-is-your-password.html
description: 
license: CC BY
---

After last month's article about
[what constitutes a weak password](https://orbitalflower.github.io/20150328-stop-numb3r1ng-up-passwords.html)
and Edward Snowden's advice on
[how to make a strong password](https://www.youtube.com/watch?v=yzGzB-yYKcc),
it's worth exploring how exactly to quantify a password's strength.

Rules like "must contain a number, a capital and a symbol" _tend_ to create
stronger passwords, but the only true measure of its strength is how well
it stands up to brute force attack.

## More cowbell

The strength of a password depends on the number of guesses, on average, which
must be made in order to find the correct password.

You're essentially hiding a needle in a haystack. There are only three ways to
do this better:

1. Don't tell anyone where you hid the needle. In fact, don't even tell anyone
   which haystack it's in.
2. Don't pick an obvious or predictable place, because they'll look there first.
3. Use a bigger haystack, so it takes an impossible amount of time and they
   give up.

A strong password must therefore have three properties:

1. __Secret__: If known to an adversary, the password's strength is reduced
   to zero.
2. __Random__: If it follows a predictable pattern, an adversary who can bias
   their guesses toward passwords adhering to known patterns can find it
   sooner.
3. __Drawn from a large set__: A password which only uses lowercase characters
   is weaker than one which also uses uppercase and numbers, since more
   variety means a much wider guessing pool; likewise, longer passwords have
   more possible values and are stronger.

## Password entropy

If chosen completely at random, the odds of guessing a password in one try
are equal to the number of possible values it can have. This is known as
information entropy or password entropy and is typically a very large number
represented as a power of two.

Password entropy like this is widely considered the most accurate way to
calculate the strength of a password.

A simple way to calculate this is to calculate `log(c**n,2)` where
`c` is the size of the character set and `n` is the number of characters in
the password. We can say, for example, that a password of eight lowercase
alphabetic characters 26<sup>6</sup> possible combinations and thus has an
entropy of `log(26**6,2)`, or approximately 2<sup>28.2</sup>, also called
__28.2 bits of strength__. Each lowercase letter in the password adds
approximately 4.7 bits of strength, allowing easy calculation.

We can also use things that aren't characters: for example, the Diceware system
uses words picked at random from a list of the 7,776 common words. Each word
from a list of this size adds approximately 12.92 bits of strength.

| Character set                  | Size  | Entropy |
|:------------------------------ | -----:| -------:|
| Digits (0-9)                   | 10    |   3.32  |
| Hexadecimal (0-9, a-f)         | 16    |   4.00  |
| Lowercase (a-z)                | 26    |   4.70  |
| Punctuation                    | 32    |   5.00  |
| Lowercase + numeric (a-z 0-9)  | 36    |   5.16  |
| Upper + lowercase (a-z A-Z)    | 52    |   5.70  |
| Alphanumeric (a-z A-Z 0-9)     | 62    |   5.95  |
| Base64                         | 64    |   6.00  |
| Alphanum + punctuation + space | 95    |   6.57  |
| [DuckDuckGo passphrase](https://duckduckgo.com/?q=passphrase+4+words) wordlist | 4293 |  12.06  |
| [Diceware](http://world.std.com/~reinhold/diceware.html) wordlist | 7776  |  12.92  |
| [xkcdpass](https://github.com/redacted/XKCD-password-generator) wordlist | 65355 |  16.00  |

For the password to have the required strength, the attacker must not predict
it in a more reliable pattern. For example, the word "boat" as four lowercase
letters is technically 18.80 bits, but if the attacker uses something like the
Diceware word list, its value is reduced to 12.92 bits.

If a password is made from randomly chosen alphanumeric, each digit is
worth 5.95 bits since the attacker has no way of predicting whether any given
character will be a digit or not. However, digits added to the end of a word
are likely to be predicted, and both the word and the digits are worth no
more than their base values.

Gimmicky, highly predictable modifications add very little:

| Modification                | Entropy |
|:--------------------------- | -------:|
| Initial capital             |    1.00 |
| Exclamation mark at end     |    1.00 |
| Leetspeak (per valid char)  |    1.00 |
| Leetspeak (all valid chars) |    1.00 |

## Sample password strengths

### Weak passwords

[RFC 4086](https://tools.ietf.org/html/rfc4086#section-8.1) recommends
a password with at least 29 bits of entropy for online services that use
rate limiting on login attempts. Anything less than this should be
considered weak and never used as a password. For example:

| Password format              | Example    | Entropy |
| ---------------------------- | ---------- | -------:|
| 4 digits                     | 8017       |   13.29 |
| Common word (Diceware list)  | boat       |   12.92 |
| Obscure word (xkcdpass list) | younglings |   16.00 |
| Common word + 2 digits       | boat80     |   19.59 |
| Two words                    | niceboat   |   25.85 |
| 6 random lowercase           | bceucx     |   28.20 |

### Moderate passwords

Passwords of about 40 to 64 bits are reasonable on an online system with
a rate-limited login and two-factor authentication. They are __not__
suitable for Wi-Fi passwords, securely encrypting files, or anything
else where a hacker can directly attack the system.

| Password format              | Example             | Entropy |
| ---------------------------- | ------------------- | -------:|
| 3 random words               | shedboatmuseum      |   38.77 |
| 10 hexadecimal               | 9d3a7b40ba          |   40.00 |
| 3 words, 2 chars leet\*      | appletr33bike       |   46.77 |
| 3 words, 3 leet, capital\*\* | Appletr33b!ke       |   47.77 |
| 4 random words               | shedboatmuseumhouse |   51.70 |
| 10 full alphanumeric         | +>7F'fBp"O8         |   59.54 |

\* UK government [Cyberstreetwise](https://www.cyberstreetwise.com/passwords) website calls this a "medium" password.

\*\* UK government inaccurately calls this a "strong" password.

### Strong passwords

Passwords of 75 to 96 bits are highly secure. The
[Diceware FAQ](http://world.std.com/~reinhold/dicewarefaq.html)
recommends at least 75 bits, but ideally 90 bits or more are necessary
to protect against highly advanced attackers or near-future threats
(e.g. exascale computing).

| Password format      | Example             | Entropy |
| -------------------- | ------------------- | -------:|
| 6 diceware words     |                     |   77.55 |
| 5 xkcdpass words     |                     |   80.00 |
| 16 alphanumeric      | 3g2upl4pq6kufc4m    |   82.72 |
| 16 base64            | QNodNwuykckjzU+m    |   96.00 |

### Very strong passwords

128-bit keys are the gold standard for banking encryption and data storage.
Passwords of this strength are difficult to remember, but when using a password
manager to create and store passwords, there's no reason to use weaker than
this.

| Password format      | Example                      | Entropy |
| -------------------- | ---------------------------- | -------:|
| 8 xkcdpass           |                              |  127.97 |
| 10 diceware          |                              |  129.25 |
| 22 alphanumeric      | vVExmhndBg184F8MzxoSmJ       |  131.00 |
| 20 full alphanumeric | iOt$bc8c7tU7m[-u+yXF         |  131.40 |
| 28 lowercase         | kpkqafwfoyurzdztulvbakyxphjw |  131.61 |

## Weaker without randomness

All this said, __humans choose more predictable passwords than computers__.
For a password to have the estimated strength it must be
chosen __completely at random__, whereas most human-picked passwords have
some bias (e.g. you pick certain digits more than others, use meaningful
words instead of random letters, write sentences that makes sense, etc).

Meaningful __passphrases__, while memorable, are weaker than their pure
wordcount. Such passphrases are still recommended by some experts (Edward
Snowden, Nadim Kobeissi) because their length means they're still quite strong.
However, their practical strength is more complicated to measure. It's stronger
to pick words at random, and then make them memorable by thinking of some
mnemonic.

## Don't rely on passwords

Ultimately, passwords are a trade-off between memorable and secure. The
human element introduces weakness that's difficult to factor out of the
system.

The simplest and most effective password advice is to use a moderate or
strong password with a second factor for your main e-mail account, then
use a password manager to store extremely strong computer-generated
passwords for everything else.
