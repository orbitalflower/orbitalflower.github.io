---
title: "Password length beats password complexity"
category: comp
tags: security
redirect_from:
- 20151012-password-length-beats-complexity.html
description: 
license: CC BY
---

[The latest MalwareJake
article](https://malwarejake.blogspot.com/2015/10/why-is-length-complexity-because-math.html)
is entirely correct: password length is more significant than its complexity or
character set.

The EFF's Christopher Soghoian gives [a good
example](https://twitter.com/csoghoian/status/653222525128810496): twelve
characters lowercase is better than eight characters of lowercase, uppercase and
digits. This is a significant usability improvement if you have to type a
password on a smartphone.

A twelve character password made from the 26 lowercase letters has
26<sup>12</sup> possible combinations, equal to about 95,429 trillion or
approximately 2<sup>56.4</sup>. An eight character password made of the 62
lowercase, uppercase and digit characters has 62<sup>8</sup>, which is only
about 218 trillion or 2<sup>47.6</sup>.

Mathematically, adding length to a password generally increases its space more
than extending its character set. The simplest way to look at this is to
consider a digits-only code such as a PIN.

A single digit has 10 possibilities: from 0-9. Adding a second digit multiplies
it by 10, for 100 possibilities: this is clear if you notice it can produce any
code from 00-99. A six digit code likewise has 10<sup>6</sup> or one million
possibilities, from 000000 to 999999. Each additional digit makes the PIN code
10 times stronger.

Suppose that we change from digits to letters. A six letter code has 308,915,776
possibilities, a more than 300x improvement. But if we instead used a 10 digit
code, we could have 1,000 million. The additional 4 digits, obviously having
1,000 possibilities, give a 1,000x improvement over six digits.

When it comes to lowercase passwords, four random letters have 456,976 unique
combinations, and adding them to a password improves its strength by 456,976x.

But for an 8-character password, increasing it from lowercase to lowercase,
upper and digits improves the strength by only about 1,046x.

The significance of the character set improves exponentially with the password
length. You have to reach 15 characters before swapping the character set from
lower to upper-lower-digits matches the strength of just adding four lowercase
characters.

Even then, you find that increasing the length 26.67% is equivalent to
increasing the character set by 238%. It's clear that the exponent, the length,
is typically more significant.

Uppercase in particular tends to be harder both to type on a smartphone and to
remember phonetically. The password segment "NgGQ" would be spoken "uppercase N
g uppercase g uppercase q", requiring seven "tokens" to encode four characters
unambiguously. Adding upper and digits to a lowercase password effectively
increases the spoken length by about 42%, so that the 8-char upper-lower-digits
and the 12-char lower password are almost equally "long" in human memory.

In that regard, the Diceware system recommends mentally encoding punctuation in
single-syllable form for ease of memory. Thus the password fragment "4@\n&"
could be pronounced "four at back n and". However, there is no equivalent set of
single-syllable names to distinguish the uppercase letters. Tonal difference,
perhaps: mentally speak uppercase as high pitched and lowercase as low pitched.
This is probably more difficult and more fallible than just remembering another
four letters.

It should be noted, however, that all of these rules apply only to randomly
selected passwords. If your letters form a recognisable pattern, such as the
first letter being a capital or the letters forming a word, all bets are off. As
I've written before, "boat" is not 1 in 456,976 for four letters, but more like
1 in 10,000 as a common English word.

The MalwareJake article recommends long passphrases, which in general is a great
way to get 20+ character password length without compromising strength. While
one word is weak, length is king, so that four words are quite strong and eight
words practically unbreakable today.

However, the example passphrases in that article are human-chosen, semantically
correct complete sentences. To a particularly advanced attacker, this makes them
easier to break than the XKCD style of choosing completely random words and
forming a mnemonic afterward.

Take the password "iwanttorideahorse". If the attacker guesses that the second
word is "want", he knows there's a high likelihood that the rest of of the
password is "i want to (verb) a (noun)", and that the verb will be something
normal to do with the noun. It's easy to remember but weaker against this kind
of analysis than a meaningless phrase like "correct horse battery staple".

But right now, lexical analysis of passwords is not commonly used. A 17
character password, even if your attacker presumes all lowercase, is about
2<sup>80</sup> variations, which is "supercomputers 20 years from now"
territory. It's weaker to an especially intelligent attack but even then, as
long as it's sufficiently original (i.e. not a song lyric, catchphrase or a
phrase you say a lot), your meaningful passphrase will still resist most attacks.

By comparison, a six character password can be broken in minutes on a low-end PC
today, regardless of complexity.
