---
title: "Age verification is identity verification—and worse"
category: opinion
tags: privacy
description: "Age verification systems are more than what they seem: identity verification, DRM, censorship, and more."
license: CC BY
---

In old hacker slang, to take adverse control of a computer system is to "own"
it. The implication is that the buyer of a computer is normally its
administrator, and has full authority to decide what software operates and what
it does. The hacker who subverts that power makes themself, in effect, the
system's owner.

Naturally, this is a serious crime, with a few exceptions. It's not illegal for
the government to do it, assuming they follow their own laws. Corporations often
make software worse, to which one counter is free and open source software. And
children, particularly the
[iPad kid generation](https://en.wikipedia.org/wiki/IPad_kid),
are used to having Internet safety settings enabled on their device.

We call the last category "parental controls," because the assumption is that
they are enabled only for children, and at the discretion of their parents. It's
been an option for about as long as the Web has existed, but it's always been
something the owner ultimately has control over.

Some 30 years later, a radical new set of laws is undermining that assumption.
ID-based age verification systems are being made mandatory, enforced by OS-level
control systems. We are seeing the end of the era of _parental controls_, and
the beginning of _government and corporate controls_, marking a severe decline
in both right to privacy and our basic freedom of computing.

## Identity verification

__There is no way to prove your age without also revealing your identity.__

A major salvo in the war on privacy landed in 2025, when the UK's Online Safety
Act required websites to verify the age of users. UK telecoms regulator OFCOM
defined a narrow set of age proofs: in practice, photo ID, credit card (not
debit card), or turning on the user's camera. All require the user to reveal
their identity.

Fundamentally, it's not possible to prove your age without proving to someone
that you are _you_.

For decades, the preferred solution has been to assume everyone was an adult
unless someone in their household chooses to enable parental controls. It's
discreet, preserves user privacy, empowers families to make decisions about
appropriate content, and works even to block sites which resisted control.

This is insufficient for governments, who wish to know, for any given post, how
to trace it back to an individual; and corporations, who profit greatly from
collecting your personal information like they're trying to get all the Pokémon.
Anonymity has always been part of the Web, but it disempowers authoritarianism,
and it's not so profitable.

## Freedom of computing

The most extreme new law, soon to be adopted no doubt by everyone, is the
requirement that age verification be baked into every operating system.

As a Linux user for many years now, I was surprised to learn that Windows users
nowadays require a Microsoft Account to log into their own PC. Bad luck if your
country is embargoed by the United States, or you're a prosecutor at the
International Criminal Court&mdash;your your PC has been "owned" by governments
and corporations.

Now, corporate control is coming for everyone else. California recently passed
such a law, and UK users report that iOS 26.4 also requires age verification.

By default, all operating systems&mdash;desktop PC, mobile, or
whatever&mdash;must now assume you're a minor, unless you submit to age
verification, and are able to pass it, _and_ your operating system implements
the feature. Every operating system pre-2026 is non-compliant, as is every open
source operating system.

It's easy for Microsoft and Apple to accept the financial costs of running
verification systems, but how should Linux do it? Who pays the verification cost
for every user? Does Ubuntu have to run its own verification server? Does Mint
need its own, or can it piggyback on Ubuntu's? What about a user account shared
by multiple people? What about servers?

What if I'm logged in as root&mdash;who verifies for the root account's age?
Does a bot or daemon have an age? If Linux refuses to comply, will it be banned
from millions of servers? What about systems which do not require a user
login&mdash;do I have to turn in my Nintendo DS? My Commodore Amiga?

Even storing the date of birth of a user involves revealing personal
information, something which under EU privacy laws is a controlled substance.

## Digital Rights Management

I don't know anyone who appreciates DRM. A game that requires a constant
Internet connection to make sure you aren't pirating it; a video you can't watch
in VLC because of anti-piracy encoding; a movie you can't play on your
region-locked DVD player.

How much worse now that movies, software and video games are to be _age
locked_&mdash;and, given the strict verification requirements required by law,
_ID locked_?

It is not illegal to play a video game for which you do not meet the PEGI or
ESRB rating. They're recommendations, not law. Some countries forbid the sale of
age-rated games to underage customers, but you never needed to show photo ID to
your DVD player before watching a movie, or have your Wii photograph your face
and sent it to Nintendo before you could play _Resident Evil 4_. Your mother
could always let you stay up to watch a scary movie if she thought you were
mature enough.

UK users of Digital game distribution platform Steam must now prove their age by
[linking a credit card](https://www.newsbeep.com/uk/105422/)&mdash;perhaps the
least intrusive identification method, for a service whose main use case is to
handle credit card payments anyway. But no other verification methods are
permitted&mdash;no exceptions are made for users whose Steam accounts were
created more than 18 years ago! Consider how much worse it will be when it is
built-in at the OS level.

## Censorship

There's a _Star Trek_ episode where the crew inadvertently offend an alien
ambassador whose culture considers the act of eating to be obscene. Eating, like
defecation and procreation, is a natural part of life, but one which his
species finds so shameful that it may only be done in private, and never spoken
of.

In a free society, adult content is legal, and even protected by freedom of
speech laws. This makes it difficult to ban entirely, much to the chagrin of
some religious fundamendalist groups. However, it is possible to damage the
adult entertainment industry in other ways, such as lobbying the government
to engage in over-regulation.

Age verification is expensive. Verification services charge as much as $0.30 per
user, enough to shut down non-profit sites, and substantially increasing the
cost of user acquisition. Existing sites must effectively ban all their users
until they verify. Even a small forum of 2,000 active users may be billed $600,
more than a month's hosting costs, and not a negligible amount.

Static personal homepages, or legacy forums without an easily implemented age
verification API&mdash;as I've complained in the past, most such sites never
even developed to the tech level of OAuth or passwordless login&mdash;will be
unable to comply.

On top of this, you lose users who want to browse quickly and discreetly without
making an account, which is one of the primary use cases of free adult sites.
Age verification also forbids millions of adults who don't have ID or can't get
a credit card. You don't have to outlaw an industry if you can make it
unprofitable.

In a second flanking attack, Visa and Mastercard have been asserting their
authority by forbidding the use of their cards on sites which sell adult
content, or certain categories of legal content which they desire to censor, for
mystery reasons. In other words, both paid content and the free ad-supported
model are under attack.

The third blow is that if a site becomes fully login-only, it's gone from the
[surface web](https://en.wikipedia.org/wiki/Surface_web), a term referring to
the the pages indexable by search engines and readily available to users. Adult
content becomes invisible and unaccountable to the public.

Many sites will have to respond by banning adult content entirely, and this is
ultimately the goal: divide the Web into a clean work-safe service, and a seedy
underbelly of signup fees and ID checks. As with movie and music piracy, this
will surely push consumers into the dangerous and unregulated black market of
filesharing tools and dark web sites, where the law is not well enforced.

## Conclusion

Of course, it's not just about adult content. Like the alien ambassador who is
ashamed to admit in public that he _eats food_, this is just a weak point that
respectable politicians are less willing to defend. They ought to, because you
would absolutely rather your constituents get their adult content from _RedTube_
than the Dark Web.

Laws, or proposals, also ban under-16s from social media&mdash;again, banning
adults who are unable or unwilling to provide ID, and shutting down smaller or
less financially stable social media sites. The UK intends to do the same to
VPNs, given that 70% of the country is now using them, in part to circumvent
verification requirements that nobody needed or wanted in the first place.

This is unprecedented overreach. Against the will of the people, governments
worldwide are implementing something akin to parental controls, except that the
arbiter is not the owner of the device or their parent, but government and
corporations&mdash;in other words, _government controls_ and _corporate
controls_.

## Further reading

- [Age verification isn't sage verification when it's inside operating systems](https://www.theregister.com/2026/03/16/opinon_column_age_verification/) - The Register
- [Age-Verification and the World Before Social Media](https://hackaday.com/2026/03/24/age-verification-and-the-world-before-social-media/) - Hack a Day
- [California's Problematic attempt to add Age-Verification to Software](https://hackaday.com/2026/03/05/californias-problematic-attempt-to-add-age-verification-to-software/) - Hack a Day
- [DoesItAgeVerify](https://github.com/BryanLunduke/DoesItAgeVerify) - A list of which Linux distros do or do not intend to implement age verification.
- [FAQs a million](https://www.cyberleagle.com/2025/09/faqs-million.html) - Cyberleagle
- [How to Give the Government New Power to "Un-Person" Someone, In Three Easy Steps](https://www.aclu.org/news/privacy-technology/un-personing-with-digital-id) - ACLU
- [Six Questions to Ask Before Accepting a Surveillance Technology](https://www.aclu.org/news/privacy-technology/six-questions-to-ask-before-accepting-a-surveillance-technology) - ACLU
- [Social media age verification laws by country](https://en.wikipedia.org/wiki/Social_media_age_verification_laws_by_country) - Wikipedia
- [The EFF Nails It: What's Wrong with UK Digital ID](https://hackaday.com/2025/12/09/the-eff-nails-it-whats-wrong-with-uk-digital-id/) - Hack a Day
- [The web should remain anonymous by default](https://blog.mozilla.org/en/privacy-security/web-anonymity/) - Mozilla Blog
