---
title: "UK spy agency recommends using weaker passwords"
category: opinion
tags: security
redirect_from:
- 20150922-uk-spy-agency-recommends-weaker-passwords.html
description: 
license: CC BY
---

British spy agency GCHQ this month issued a Guidance recommending that citizens
[stop using strong
passwords](https://www.gov.uk/government/publications/password-policy-simplifying-your-approach/password-policy-executive-summary).

CESG, the GCHQ department who issued this advice, admits that this goes against
popular advice, including their own previous guidance. I disagree significantly
with this new article: until we live in a post-password era, [strong
passwords](https://orbitalflower.github.io/20150328-stop-numb3r1ng-up-passwords.html)
are necessary for good security.

Further, GCHQ's increasing role in attacking civilian systems (e.g. the Gemalto
hack) reveals a considerable conflict of interest. This new advice should be
subject to scrutiny.

## Downplaying the threat of password attack

The article suggests that "complex passwords do not usually frustrate
attackers", and describes nine methods attackers use to break passwords. As I
said in [When can you use a weak
password?](https://orbitalflower.github.io/20150517-when-can-you-use-weak-password.html),
when the attacker has immediate access to the password, its strength is
irrelevant.

However, CESG downplays the threat of non-immediate password attacks, especially
brute force attacks. Passwords of at least moderate strength are necessary to
protect against remote login attempts - a weak password is like as a wall made
of cardboard. In the case of Wi-Fi brute force or leaked password databases,
a high-end consumer PC can break even moderate passwords within days.

## Admitting this advice is weak

CESG admits that their advice against strong passwords is inappropriate in many
situations: "It is not intended to protect high value individuals using public
services."

What this means is that weak passwords are insufficient to protect your online
accounts from a determined attacker. This is absolutely correct. In fact, the
article even lists hacked user databases (such as from hacked websites) as a
threat to discover passwords.

Weak passwords, the article suggests, are only secure on the assumption that
they're used within a business whose IT infrastructure is strong enough to keep
out attackers in the first place.

## Discourages password managers

Password fatigue is a significant problem, but the article is vague on how to
help users deal with this. For example, it suggests "technical solutions to
reduce the burden on users", but warns that password management software
"carries risks". What technology, then, is appropriate?

Securely recording passwords is perhaps reasonable, but without software this
needs be done either in some kind of hardware (rare) or on paper. But this goes
against the introduction's warning that writing down passwords carries greater
risk than using weak passwords. In any case, once the user no longer needs to
commit passwords to memory, strong passwords are no longer difficult to use.

The theme of this article seems to be that passwords are bad, primarily due to
password fatigue encouraging poor password hygiene that leads to weaknesses in
security. So it's strange that one solution is to not use passwords at all
unless necessary.

There's no mention of single-sign-on systems to allow users to authenticate to
the entire system with only one password, which the minimum number of passwords
a user can have unless you use some alternative authentication technology.
There's no mention of these alternative authentication technology either, except
for a vaguely described "technical solutions". No mention of OAuth, FIDO U2F or
biometric authentication.

## Weak password advice

CESG correctly identifies that user-generated passwords tend to be weaker than
machine-generated ones, and their advice to use passphrases or XKCD style four
random dictionary words is commendable. Depending on your wordlist, a four-word
password might have a strength of between 48 bits ([DuckDuckGo
wordlist](https://github.com/duckduckgo/zeroclickinfo-goodies/blob/master/share/goodie/passphrase/words.txt))and
64 bits ([xkcdpass
wordlist](https://github.com/redacted/XKCD-password-generator/blob/master/xkcdpass/static/default.txt)).

However, the third recommendation of CVC-CVC-CVC style passwords is rather weak.
It's only nine characters, forms a highly predictable pattern, and is harder to
remember than three actual words, which would be more secure. Each
three-character set has only 2,205 possibilities, around half as many as the DDG
wordlist. If the attacker knows or guesses the password format, which he can do
by seeing even one expired password, each password has an equivalent of only
33.32 bits entropy, slightly weaker than a six character alphanumeric password
or a three word DDG passphrase.

## Suggests throttling is unnecessary

The article wisely recommends account lockout and throttling of login attempts,
which if correctly implemented will make even a moderate password secure. What's
surprising is that it also recommends "protective monitoring" as an alternative
to these, rather than an addition. This would allow an attack to take place
first and only warn later.

There is the possibility for either machine failure or human error to fail to
spot a repeated access attempt, and the relatively small problem of password
lockout is not worth abolishing an entire line of defence.

It also suggests that the method of protecting user credentials should be
specified in any outsourcing contracts, but this could potentially leak the
security measures to outside the company, which removes a line of security by
obscurity.

## Vague on password storage requirements

While it's well-established that passwords should never be stored in plain text
and the secure storage of passwords today is [well
understood](https://www.nccgroup.trust/us/about-us/newsroom-and-events/blog/2015/march/enough-with-the-salts-updates-on-secure-password-schemes/),
the advice CESG gives is somewhat shaky, considering that GCHQ has many of the
world's best cryptographers and security specialists.

It recommends hashing passwords with SHA256, which is insufficient on its own;
[benchmarks](https://hashcat.net/oclhashcat/#performance) break it at 355
million per second on a standard desktop PC. The same list simultaneously
recommends PBKDF2 by name, which is one of the easiest to implement poorly,
giving weak security with the illusion of strong security - precisely what an
advanced persistent threat needs to gain access.

And while it recommends PBKDF2, it doesn't make mention of bcrypt or scrypt,
both considered strong. Nor does it even mention work factors, which make the
difference between feeling secure from brute force and actually being secure. It
simply recommends SHA256, PBKDF2 and salts, a definition which is not in itself
enough to secure passwords from any moderately advanced threat.

But the most insane advice in the entire is the suggestion to regularly search
for passwords to ensure that they aren't being stored anywhere in plaintext.
This will involve sending the passwords themselves in plaintext over the
network, which can be intercepted, or search the machines, which will now store
it in their search history, which will be saved to disk and potentially
available to an attacker from discarded disks or even a single password.
Thankfully, this is quite difficult to employ if the passwords are stored
hashed.

## Conclusion and advice

Please, continue to use strong passwords until such times as passwords are
obsolete. For personal online accounts, of which you may have more than fifty or
a hundred, use a password manager. Yes, your PC can be hacked, but an attacker
who can do this could just keylog your password anyway. It's more probable that
one of the many sites you use will be hacked, in which case the only defence is
very strong computer-generated passwords, unique for each site, and a password
management system is the only way to do this.

For your important accounts, especially your e-mail which you cannot afford to
lose since it unlocks all your other accounts, enable two-factor auth - it
will often save you even when an attacker gets your password.

## Addendum

There appears to be an interesting link between CESG and the Cyber Streetwise
government website, whose password advice I commented on back in March. The
guidance article issued by CESG and CPNI went live on the 8th of September,
while Cyber Streetwise updated their password advice page to include a new
Youtube video uploaded on the 5th of September.

This is interesting, since while the Cyber Streetwise site is led by the
government's Home Office and Cabinet Office and boasts the National Crime Agency
as one of its partners, there's no mention of how they're involved with CPNI,
CESG or GCHQ.

At any rate, the password advice that I was critical of has changed recently.

The original site recommended three or more random words, using both upper and
lowercase, numbers and symbols, but incorrectly claimed that [l33ting up
passwords](https://orbitalflower.github.io/20150328-stop-numb3r1ng-up-passwords.html)
was effective at improving password strength. It emphasized the importance of
protecting your e-mail account, avoiring personally identifiable information,
and using unique passwords for each account. It recommended four ways to
remember passwords: imagining objects in a location, imagining words in a story,
building an acronyms from famous songs, and password manager software.

The new webpage drops several of these recommendations. It correctly no longer
advises l33t-ing up passwords or song lyric acronyms. Unfortunately, it also
drops the recommendation to use unique passwords on each site, and no longer
recommends password manager software. Both are in line with the recommendation
CESG's advisory made three days later, even though that advisory says those
guidelines are insufficient to protect users on public websites.

The new guidelines also make the subtle change from recommending "three random
words or more - the longer it is, the harder it is to crack" to "simply choose
three random words... using three random words is the key to creating a strong
password". An accompanying diagram shows a passphrase created from three related
words, which are easier to crack than three actually random words. The site
offers mnemonics for remembering random unrelated words, but doesn't explain how
to generate such strong passwords and actively removed advice on password
management software which is capable of secure password generation.
