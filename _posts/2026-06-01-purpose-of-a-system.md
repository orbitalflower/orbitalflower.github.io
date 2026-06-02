---
title: "The purpose of a system is what it does"
category: opinion
tags: privacy censorship
description: "back on my censorship rant again"
license: CC BY
last_modified_at: 
---

There's a [hit tweet](https://x.com/primawesome/status/1178671690261286918) that
goes as follows:

> My neighbor told me coyotes keep eating his outdoor cats so I asked how many
> cats he has and he said he just goes to the shelter and gets a new cat
> afterwards so I said it sounds like he’s just feeding shelter cats to coyotes
> and then his daughter started crying.

Wikipedia has an article on this concept, titled
[The purpose of a system is what it does](https://en.wikipedia.org/wiki/The_purpose_of_a_system_is_what_it_does).
It's a cynical and seemingly irrational attitude, but at some point you have to
look at the functioning of a system and ask whether you've built a
coyote-feeding machine.

Yes, I'm back on my anti-censorship rant again.

## The failure of age verification

I've previously ranted about the
[Online Safety Act](../opinion/online-safety-act-bad.html), a British law which
is ostensibly about child safety, but has disastrous side-effects for everyone
else.

In short, the OSA ignores the plethora of existing online safety tools,
especially parental controls, which are so well trusted that parents felt safe
allowing unsupvervised internet access to an entire generation of children, the
"iPad babies". Instead, OSA requires all existing websites, the vast majority of
which are based outside the UK and cannot be forced to comply, to implement
[age verification](../opinion/age-verification.html).

Only a very limited set of verification methods are permitted, all of which
violate the individual's privacy. They are cumbersome enough to discourage
users, and expensive enough for the site operator at scale to undermine the
business model of free ad-supported content.

One has to wonder if _that's the point_.

## Proof of age

Suppose a British man wants to buy alcohol. He carries his purchase to the
self-service checkout and scans it, where a staff member glances to confirm the
gentleman's appearance before swiping approval. No record is made of the buyer,
nor any imposition made upon him. His counterpart in the United States is more
likely to be made to show ID (such is the cost of living in the land of the
free), but even then the cashier only glances at the date field, which he has
forgotten by the time the customer has left the store.

Next, he wants to visit a website featuring adult content&mdash;a much safer
pastime, given that alcohol kills nearly 10,000 people in Britain each year
([source](https://www.ons.gov.uk/peoplepopulationandcommunity/healthandsocialcare/causesofdeath/bulletins/alcoholrelateddeathsintheunitedkingdom/registeredin2024)).
Our man has already disabled the built-in adult content filter on his wi-fi hub
or at his phone network, and last week was forced to present government
identification papers to continue using his own iPhone. Today, he faces new
inconvenience: he must create an account on the adult site to prove his age.

Now comes the humiliation ritual. He must switch on his device camera and make a
little performance. Turn your head on command so we know you're not a
recording&mdash;the provider is fully aware of the potential for such a bypass.
Open your mouth. Close your mouth. Open your mouth again so you can _watch
porn_.

Who would buy alcohol in the supermarket if that were the harrowing procedure?

## Failure states of the system

A gating system fails in one of two ways: when it fails to deny someone who
should not have access, and when it fails to allow someone who should have
access.

### Fail deny modes

A major failure is when the system locks out the people it was intended to let
in; in this case adults. Going foward, as legislation passes in other countries,
this will affect more people, as well as non-adult services like social media
and computer operating systems in general. (Remember that adult content is often
used as a wedge in censorship and control, as fewer people will openly defend
it; the legal precedents it sets and systems it creates will soon come for
everyone else.)

The first failure mode is lack of support. Most sites implement only one of
three approved methods: camera-based, government ID (or combination of camera
and ID), or credit card. Most use a third party verification service, who in
most instances is some new startup not backed by a trustworthy brand.

The second is that implementing camera or ID kills the operating model or
financial viability of many sites. Camera/ID verification current costs thirty
cents, and is reliant on the continuing cheap availability of AI or underpaid
third-world workers, neither of which are guaranteed going forward. Video
advertising pays in the range of 0.1 to 0.5 US cents per view. Transactional
verification is non-viable for ad-supported sites, so users have to sign up.

Any obstacle to signup on a site also decreases engagement. Recall the professor
who saw reduced sales after moving his book from Amazon to a site where most
people didn't already have accounts. The intentionally signup-free experience
was one reason 4chan grew faster than competitors, and once appeared in Alexa's
top 100 US sites. Recall how when Amazon was an online bookstore, free shipping
resulted in increased sales, except in France, where the shipping 1 Franc (US
$0.10); the psychological distance between free and any amount of money is
_huge_.

Even credit card payment imposes a barrier to entry. Credit cards are the least
privacy-harmful option by a small margin, but are only readily available to the
successful in our society. If you are poor, unemployed, or have no credit
history, you cannot acquire a credit card, and therefore cannot use any site
which uses credit card authentication only. This is bad for you and for the
site.

Another huge category of failure modes is when the site can reliably determine
that an individual is an adult, but by means not approved by the government.
Account age is forbidden as an identifier. Zero-knowledge proofs were known of
when the OSA was drafted, but not included. Each site pays the verification fee
each time, rather than consulting a common service; a service could validate and
sign a PGP key or similar, but this was not considered.

### Fail allow modes

The real stinker is that age verification is so trivially bypassed that it
doesn't even fulfil its stated purpose.

Some sites will not comply, to begin with. We must therefore continue to use the
existing parental control systems, rendering the age verification systems
redundant.

Even so, all three major ID methods are readily tricked.

1. Photo verification has been provably fooled by a variety of means, including
   drawing a fake beard on your face, capturing video from an a video game
   character, and borrowing an older friend.
2. Fake IDs are readily accessible to teenagers, who already use it to buy
   alcohol and tobacco.
3. Credit cards can be borrowed, sometimes under fake pretexts, perhaps from an
   older friend or relative. This issue came up
   [in July 2010](https://games.slashdot.org/story/10/07/06/1823202/blizzard-to-require-real-first-and-last-names-for-official-forums),
   when Blizzard started requiring real names and it was noted how many _World
   of Warcraft_ players used their mother's credit card.

In all cases, account sharing is trivial and socially accepted as a concept.
Identity verification to validate an _account_, rather than an _individual_, is
fundamentally broken. Verification of an individual would require a much more
invasive and persistent form of on-device surveillance, with the goal of linking
much of a person's online activity to a real identity.

## That's the point

When a system collects real-life identification, makes it hard for adult content
providers and small websites to operate, and still fails to filter out minors,
what you have is not an online safety system. What you have is an anti-porn
censorship system and mass surveillance network.

According to POSIWID (The purpose of a system is what it does), _that's the
point_.

There's a certain mindset, particular to older politicians, who fear change.
They actively seek to return us to the way things used to be, to a
pseudo-mythical past that resembles the idealized and easily-understood
narrative about the world they believed when they themselves were younger.
There is no place for Pornhub in the idealized past.

Next, the entire open, free, and anonymous Internet is anachronistic to the
nostalginauts. The idea that information of any sort can be acquired discreetly,
or that people can communicate without showing their face, is an anathema to
their worldview. The conspiracy theorists have us running frightened of
immigrants, benefits claimants, trans people, or "woke"; we should rather be
afraid of the imminent and ongoing dismantling of the World Wide Web after
thirty-odd years of freedom, which will strike us all regardless of political
alignment.

Happy Pride month, everybody.

## Further reading

- [Age verification for social media – the beginning of the end for a free internet?](https://www.mullvad.net/en/blog/2026/6/1/age-verification-for-social-media-the-beginning-of-the-end-for-a-free-internet/) - Mullvad.
  "In reality, age verification lays the foundation for a fully government
   controlled internet."
