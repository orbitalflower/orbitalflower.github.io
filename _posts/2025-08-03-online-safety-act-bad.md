---
title: "The Online Safety Act is unfit for purpose"
category: opinion
tags: privacy
description: "An article on why the UK's Online Safety Act 2023 is a bad law and unfit for purpose."
license: CC BY
---

In July 2025, the
[Online Safety Act](https://en.wikipedia.org/wiki/Online_Safety_Act_2023)
came into force in the United Kingdom. Marketed to the public as a novel way to
protect children, it was immediately shown to be ineffective at its stated goal,
and with disastrous side-effects. It is a badly designed law, and unfit for
purpose.

1. Table of Contents
{:toc}

## Ulterior motives

We have, as a society, almost completely forgotten about the Edward Snowden
whistleblower leaks of 2013. In 2015 he was 
[smeared by the Sunday Times](/opinion/that-sunday-times-article-on-snowden.html)
as a Russian defector, and falsely blamed for the unrelated OPM hack, a failure
of US intelligence that took place after Snowden left the NSA. In reality, he
revealed mass violations of citizen privacy by the US and UK governments, many
of which were ruled illegal following their disclosure.

One such disclosure was a program by the UK's GCHQ named
[Mastering the Internet](https://en.wikipedia.org/wiki/Mastering_the_Internet),
a project a with a budget of over £1 billion, allowing Britain to wiretap,
record, [and exploit](https://www.washingtonpost.com/opinions/no-place-to-hide-by-glenn-greenwald-on-the-nsas-sweeping-efforts-to-know-it-all/2014/05/12/dfa45dee-d628-11e3-8a78-8fe50322a72c_story.html)
all internet traffic. GCHQ's technology was used not just for national security
purposes, but [industrial espionage](/opinion/of-course-britain-does-economic-spying.html)
and such minor crimes as 
[littering and TV license fee evasion](https://www.belfasttelegraph.co.uk/news/northern-ireland/bbc-uses-ripa-terrorism-laws-to-catch-tv-licence-fee-dodgers-in-northern-ireland/30911647.html).

And this is just the systems which already passed. In 2012, Theresa May (then
Home Secretary) introduced the 
[Draft Communications Data Bill](https://en.wikipedia.org/wiki/Draft_Communications_Data_Bill),
which would have required internet service providers to record all user activity
and turn it over to the government on demand without a warrant, at a cost of
£1.8 bilion. It is naive to assume that third-party companies which verify your
government-issued ID could not simply be issued a Technical Capability Notice
under legislation such as the the Investigatory Powers (Technical Capability)
Regulations, ordering them to turn over the government IDs necessary to link an
individual to an IP address and user agent fingerprint.

This is just an overview, and the UK has a long and storied history of
attempting to pass legislation violating the basic privacy and dignity of its
citizens. The public should not give the UK the benefit of the doubt here. The
only innovation of the most recent legislation is that they managed to market it
better by claiming that it is necessary to protect children. (It isn't, and it
doesn't.)

## Failure to show necessity

In claiming that the new legislation is necessary, the government is wilfully
ignoring multiple existing layers of protection which already exist.

1. The UK maintains a blocklist of websites which permit CSAM. Such sites are
rare, as GCHQ's billion-pound mass surveillance and intercept systems allow it
unparallelled capability to find and shut down such sites, as well as the UK's
strong diplomatic system which it uses to deploy legal challenges
internationally. Illegal material, specifically, is extremely well policed.
2. UK mobile data plans include an adult content filter, which must be manually
disabled. It's so trusted that having it disabled is one of the OSA-approved
methods of determining your age.
3. UK ISPs send customers home routers with built-in adult content filters,
which may disabled by the billpayer on a per-device basis specified by MAC
address.
  * When the bill was being debated, it was noted that over 60% of Wi-Fi users
    chose to disable their filter. One member of parliament claimed this was
    caused by rogue broadband engineers disabling the filter against the
    billpayer's wishes. This absurd claim ignores the fact that ISPs no longer
    deploy broadband engineers in most cases. Nearly all UK homes have been
    broadband-enabled for some time now, and ISPs only send out an install kit
    to new users; BT developed a special long thin shipping box for this purpose
    that would fit through most UK letterboxes.
4. Nowadays, all smartphones, tablet PCs, smart televisions, television set-top
boxes, games consoles, and even Netflix have a built-in parental control
systems. These are so trusted by parents that, even in the US, which has none of
these other layers of protection, parents routinely allow their children
unsupervised access to an iPad with parental control, creating a generation of
"iPad babies".
5. It has long been standard cultural practice to forbid unsupervised internet
access to children under 13, and the establishment of a US law called COPPA in
2000 established an internet-wide standard practice to forbid people under 13
from signing up to websites.
6. Every search engine features safe-search enabled by default. Our current
trend of neural network generated AI art originated in part from Google research
into image detection algorithms, a main use of which would be to aid detection
into adult content filters.
7. Numerous small methods exist, including major sites like YouTube and Twitch
which voluntarily prohibit adult content, and sites like Twitter and Reddit
which blur NSFW content to prevent showing them accidentally.

## Severe and predictable drawbacks

Wikipedia is leaving the UK in response to the Online Safety Act, pending a
legal challenge. This is just the tip of the iceberg.

Compliance with the law, even for companies which want to, is highly onerous for
all but the largest companies. The primary legislation is 250 pages, which I
recall one slimy politician downplaying as something one employee could read in
no time at all. But this is law, not a _Discworld_ novel. Your company requires
a lawyer to interpret law!

Your intern is not qualified to give legal advice. You need a lawyer familiar
with not only the legislation, but over 3,000 pages of guidance published by UK
telecommunications regulator OFCOM (promoted from phone industry oversight to
global internet censor), any relevant caselaw (of which there is none yet), and
interactions with modifiers like the Human Rights Act and European Convention of
Human Rights. They also need a full analysis of your systems to determine if
they are compliant.

The penalty for failure to obey the Online Safety Act correctly is imprisonment,
so it's not something you can afford to DIY. And if your site is non-commercial,
or otherwise cannot afford a lawyer, it is now a severe danger for you continue
to operate it. Even if you choose to risk jail, the expense of paying the
third-party ID verification company, or the time cost of manually checking every
user's ID yourself, is an unreasonable burden.

The overwhelming majority of websites are operated from outside of the UK, and
are not subject to its legislation. In 2021, the UK population was 66.9 million,
a mere 0.85% of the global population. It should not have surprised the
politicians, then, that significant chunks of the Web chose to cut off access
rather than hire a British legal team and undertake compliance procedures.

Several US-based adult sites&mdash;entirely legal in the UK, it's worth
noting&mdash;were among the first to cut off the UK, with the result of a
massive spike in the use of VPNs&mdash;also entirely legal. The government
predictably threatened to ban VPNs, in direct opposition to its own best
practices advice, published e.g. by GCHQ subsidiary CESG in 2015,
[Security considerations for common enterprise IT decision](https://www.gov.uk/guidance/security-considerations-for-common-enterprise-it-decisions),
which advises:

> "In a typical scenario we expect [...] all traffic from end user devices to
> the corporate network to be encapsulated in a VPN

Not only adult sites are affected. Wikipedia is one legal challenge away from
leaving Britain. This was entirely predictable, because a similar showdown
happened before, and Wikipedia refused to back down. Under OSA, Wikipedia could
be required to censor itself of anything the government censors at OFCOM deem
"harmful" or unsuitable for minors, beginning with photographs of nudity which
Wikipedia uses on some pages for educational purposes. It may also be required
to force all readers to create accounts before using the site, and force all
Wikipedia editors to identify themselves with government-issued ID.

For sites which chose to cave and obey the law, the effect on law-abiding adult
users was a mess at best. Discord admins were locked out of their own server.
Spotify users were required to show photo ID to continue listening to music.
Reddit blocked all its LGBT boards. X (formerly Twitter) users were blocked from
entirely lawful adult content, pending the programming of a system to handle it.

## Further implications

And there are even more serious implications.

Once adult content sites are login-only, they are unreachable by search engines.
The "surface web" will effectively be stripped of all adult content. Search
engine traffic to sites, already stolen by AI summaries, will slow to a crawl.
Sites will close due to lack of foot traffic, or be forced to convert to a
censored, work-safe version.

Those sites which remain, but submit to the ID requirements, will find that
signup requirements impede use. The Wikipedia article on
[paywalls](https://en.wikipedia.org/wiki/Paywall) estimates that 60% to 90% of a
site's traffic may be impeded by signup and payment requirements, so it is not
unthinkable that signup and government ID would likewise lead to substantial
losses in clickthrough retention.

People without government ID will be effectively banned from many sites. Perhaps
they are lucky, because inevitably, services will be hacked, with massive
privacy issues. Websites nowadays record a lot of information on users for
commercial exploitation (concern yourself with the number of websites which have
an option in the footer to request "do not sell my data"). When women's dating
app "Tea" was hacked recently, photographic ID submitted by users was easily
recovered.

Many important websites are likely to become unavailable entirely to UK users.
Archive.org, which includes the Wayback Machine, a critical resource for
accessing old websites, and one which is practically impossible to bring into a
censored state.

## Lack of effectiveness

Finally, the law as enacted doesn't even solve the problems it was supposed to
fix.

1. It does not have any new uses to prevent CSAM or online predators. The trade
in illegal material already happens on sites which operate outside of the law.
The spike in VPNs may impede law enforcement efforts (I joke&mdash;certainly
GCHQ's systems allow British police to circumvent these by watching global
endpoints). When VPNs are inevitably banned, users will move to the Tor network,
which will see a rise in casual use of the dark web, where the true illegal
material and harmful communities thrive. This is a disaster.
2. It doesn't do anything new to protect children, particularly young children,
from accidentally accessing adult content. As mentioned, there are already home
router level filters and device-level parental controls iPads and games
consoles, which are highly effective and widely trusted. The new layer is not
necessary.
3. For those who intentionally seek adult content&mdash;older teens, perhaps, or
just privacy-conscious adults&mdash;the age verification systems have been shown
to be trivially bypassable in a number of ways, including:
  - Realistic fake IDs, which young people are already readily able to acquire
    for the purpose of buying alcohol and cigarettes, and which are produced by
    organized crime.
  - Video game characters, including Norman Reedus as Sam Porter Bridges in
    _Death Stranding 2_ and Director Breen as appearing in _Garry's Mod_, are
    able to fool facial recognition algorithms.
  - IDs can be created, edited or modified using readily available software or
    AI. One could also use an AI camera filter, makeup, etc, to appear older to
    the facial recognition.
  - It would be trivial to borrow an ID from another person to pass the ID
    check. You could also borrow another person to pass facial recognition.
  - Account sharing is widely practiced with services such as _Netflix_, and
    so there is no reason to assume a single account maps to a single
    individual.
4. It's supposed to do all this while insuring that access of legal material to
adults is not impeded, but the impediments are significant.

However, if you understand that a primary goal of this legislation is to unmask
anonymous internet users, then it is highly effective. A major limitation of
government surveillance is linking an internet connection to a prosecutable
human being. Linking every internet account to a Government ID solves this, as
does seeing a real face, which can be fed into an existing facial recognition
database (with disastrous results for victims of false positives, naturally).

During debates on the bill, the government proposed a type of age verification
card which could be purchased at any corner shop for a nominal fee, requiring of
course ID to be shown as with purchasing alcohol or tobacco. This would have
preserved user anonymity from the adult site. Naturally, the government chose
not to implement this system.

## Predictions

You have no doubt seen the John Jonik comic strip recently. Uncle Sam is buying
a box marked "Control of Internet Speech", and the salesman labaled Corporate
America asks "How would you like this wrapped?"&mdash;the options are
"Anti-Terrorism" and "Protect Kids". This is not a new idea&mdash;the comic
dates back at least to summer 2001, where it appeared in 
[Alternative Press Review](https://archive.org/details/alternative_press_review_06.2/page/61/mode/2up) Volume 6 Number 3.

I am not optimistic here. I do not have a great deal of faith in the
intelligence or honesty of British politicians, or the rationality of the
British public to see through the government's attempt to claim their latest is
really about protecting children and national security.

Nor do I think other countries are much better in this regard. The EU's
[Chat Control](https://en.wikipedia.org/wiki/Regulation_to_Prevent_and_Combat_Child_Sexual_Abuse),
legislation, also proposed on the premise protecting children, would outlaw the
end-to-end encryption used by WhatsApp and Signal, something which was
originally popularized when it was discovered that governments were wiretapping
innocent civilians without suspicion or warrant. Naturally, this will mainly
harm normal internet users, since the real criminals will take the extra effort
to deploy additional layers of strong encryption.

Once a law like this is passed, it is unlikely to be repealed. Instead, it will
become the new norm. It is forseeable that OFCOM will gradually ban
non-compliant sites. The web will become a censored, pre-watershed version of
its former self.

The de-legitimisation of legitimate, legal adult websites will push users toward
illegitimate sites, including piracy sites and the dark web. Access to illegal
material will become more common and respect for censorship law will decrease,
while tax revenue from the UK's lawful adult content industry will decrease as
international users balk at ID requirements.

VPNs will become extremely popular, but security issues will arise when young
people (and cheapskates) who cannot pay for one install suspicious, disreputable
free VPNs with malware or tracking built in. Perhaps worse, we will see a rise
in the Tor browser, which is free of charge; while in principle I support this
privacy technology, it will also ease on-boarding toward illegal sites and toxic
communities. Eventually, specific VPNs will be banned, presumably ostensibly for
not doing age verification themselves, pushing even more users to Tor, and the
barrier between legal and illegal adult content will become dangerously thin.

Small, hobbyist internet sites in the UK will close, including long-standing
forums. Large platforms like Facebook, which already blocked adult content, and
can trivially afford the time and expense of complying with any legislation,
will be unaffected, and see a boost in popularity. New startups now face a
barrier to entry, which will cement the tech giants in their positions and
stifle innovation and competition.

A little-known feature of the bill also forces sites to implement technology to
scan for CSAM, including breaking end-to-end encryption, which the government
concedes is not technologically feasible. This requirement, once it comes into
force, would immediately outlaw every single communications platform on the
planet, except for those which implement the scanning technology, which will be
trivially defeated by any serious criminal. It would also mandate a backdoor in
communications apps, a loophole which we have already seen the UK gleefully use
to conduct warrantless wiretapping of innocent citizens.

Consider also the current attack on freedom of speech in the field of 18+ video
games, where handfuls of somehow highly influential activists are manipulating
credit card processors in an attempt to force games to return to the era when
they were primitive toys and the market was dominated kid-safe fare, setting the
field back by 35 years. A broader risk is that with OSA, this becomes a
two-pronged attack on adult content in general: both the paid and ad-supported
business models are under attack.

The increased government power to control and direct OFCOM, which had previously
been an independent regulator, is concerning. It will certainly be used by some
future government to censor information.

## Positive note

Despite the pessimism, there are a few positive nuggets in all this.

Newgrounds appears to have found a way to comply with OSA age verification
requirements without violating the user's privacy. Accounts above a certain age
are automatically assumed to be over 18, as are accounts which ever used a
credit card, or accounts which used a debit card (for which you must be 16) more
than two years ago. We shall see if this method holds water.

OAuth-based authentication or OpenID Connect could potentially be used as a
method of age verification, if they supply either a date of birth or just a
true/false value for whether the user is 18+ or not. There are
[various OAuth providers](https://en.wikipedia.org/wiki/List_of_OAuth_providers),
and it would not be difficult for a startup to operate a more privacy-preserving
service to avoid linking. At any rate, this may see a rise in passwordless
authentication, which would be a good thing for security overall. There's still
potential for 
[misuse of social logins](/opinion/social-logins-still-being-misused.html), but
it's something. My main concern is that people are going to accidentally log
into porn sites with their main Google account or such, but there's a
confirmation prompt, so perhaps this will be rare.

Finally, there is some amusing irony in a
[Politico article](https://www.politico.eu/article/britain-mps-charge-vpns-expenses-minister-caution-tech-jonathan-reynolds-data/)
which noted that at least two members of parliament have expensed VPNs to their
account.

## Further reading

- [No, the UK’s Online Safety Act Doesn’t Make Children Safer Online](https://www.eff.org/deeplinks/2025/08/no-uks-online-safety-act-doesnt-make-children-safer-online) - EFF
- [We Support Wikimedia Foundation’s Challenge to UK’s Online Safety Act](https://www.eff.org/deeplinks/2025/07/we-support-wikimedia-foundations-challenge-uks-online-safety-act) - EFF
- [Online Safety Act](https://en.wikipedia.org/wiki/Online_Safety_Act_2023) - Wikipedia, the (formerly) free encyclopedia
