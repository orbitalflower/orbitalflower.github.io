---
title: "What Britain really intends to ban"
category: opinion
tags: privacy
redirect_from:
- 20151102-what-britain-really-intends-to-ban.html
description: 
license: CC BY
---

There's some discussion today over Britain's latest attempt to pass a "Snooper's
Charter" law and whether or not the government still plans to outlaw encryption
and give police warrantless access to citizens' browsing history.

The Daily Mail [claims the government has 
backtracked](http://www.dailymail.co.uk/news/article-3299110/Theresa-backtracks-snoopers-charter-drops-plans-let-police-spies-internet-browsing-history.html),
a claim contested by [The Daily
Telegraph](http://www.telegraph.co.uk/news/uknews/terrorism-in-the-uk/11970391/Internet-firms-to-be-banned-from-offering-out-of-reach-communications-under-new-laws.html),
[Eris Industries](https://blog.erisindustries.com/2015/11/02/IPBill/) and even
[Edward Snowden](https://twitter.com/Snowden/status/661267531320152064).

Lets look at exactly what the government plans.

## Encryption

The Telegraph article says the bill will force companies to provide unencrypted
data on receipt of a warrant. The government was never really going to ban all
encryption, so this isn't a backtrack. What this does is make it illegal to run
a service where the company has no access to user data in plaintext.

There are a few ways you can achieve this, from a technical standpoint.

### Client-server encryption only

One is to use only client-server encryption, but disable user-to-user endpoint
encryption. This is the norm for many sites (Twitter, Facebook), and still
protects you against most outside attacks. For sites like web forums where the
service needs your data to function normally, this is the only approach that
makes sense.

But client-server encryption doesn't protect you from internal threats. Sites
are being [hacked at an alarming
rate](http://lifehacker.com/its-no-surprise-anymore-your-data-is-never-safe-onlin-1471858210),
including major companies like Yahoo and Adobe. It's such a real threat that
it's standard practice for sites to store your password in a hashed format to
protect it from hackers.

You might also want to protect your data from the company. As online advertising
decreases in value, companies increasingly look at ways to monetise or sell your
private data. Companies can make mistakes and leak data you trusted them with.

And even Britain's law enforcement and intelligence services, who insist they
will only intercept your data on a valid warrant, were caught just a few years
ago hacking into Google and Yahoo's internal systems and stealing innocent
people's private data in the greatest ever violation of the EU right to privacy
since its inception. Innocent people absolutely have a legitimate right to
protect their transmissions from interception in this manner.

### Backdoor and MitM all endpoint encryption

Blocking end-point encryption would completely ban iMessage, Facetime and
Signal. It would force WhatsApp and LINE to disable their secure messaging
features for UK users. Facebook and Snapchat have never used endpoint security
and will not be affected.

The only solution is to insert a crypto backdoor into the system and deploy
man-in-the-middle interception against all UK users. Apple cannot do this
without being noticed: if the apps continue to operate in the UK, it will prove
that they have added a deliberate backdoor.

### Ban peer-to-peer and user encryption

For the ban to be properly effective, services must be compelled to forbid users
from deploying any encryption of their own, or from enabling users to make
peer-to-peer communications that do not pass through a central server.

This would ban PGP and OTR, if the companies are forced to go this far. That
would leave UK citizens with no access to effective communications tools which
are not backdoored by their own government.

Skype originally used secure peer-to-peer communication, but when the company
was bought out by Microsoft, who it should be noted are an NSA partner, the
system was changed to go through Microsoft's servers.

## Internet history

Based on Theresa May's statements, she wants to give police and intelligence
services the ability to see metadata of Internet usage for all users without a
warrant.

This is not much of a concession. The increasing adoption of HTTPS means ISPs
already do not have access to more information than this for major sites.

Even metadata collection without a warrant is a severe violation of the privacy
rights that the UK is sworn by multiple treaties and laws to uphold. It is an
established standard that a person's privacy can only be violated with a warrant
signed by a judge and based on probable cause, not unlike the Fourth Amendment
of the US constitution.

Yet here May thinks the average innocent citizen has no privacy interest in the
list of websites they visit. No person of the Internet-savvy generation would
agree here. How many people voluntarily publish their own browsing history? When
a user enables Private Browsing mode, now a standard feature of web browsers,
it is impossible to deny that this signals an expectation of privacy.

## The usual spin

May deploys the usual GCHQ propaganda lines on the Snooper's Charter, as well as
some clever trick statements of her own.

May asserts that the new Snooper's Charter is merely "setting out the current
position, which does enable the authorities with proper authorisation to issue
warrants". This idea that the new law will not grant new powers but merely
maintain old ones is [an old
scam](https://orbitalflower.github.io/20150604-intelligence-gap-is-doublespeak.html),
used to grab powers that no nation on Earth has ever possessed in human history.

And the statement that authorities can issue warrants dodges two issues: these
"warrants" are often signed by cabinet ministers or civil servants instead of
judges and are not true warrants at all; and new powers will also be granted
without even these weak pseudo-warrants.

"Proper authorisation" is a completely meaningless term in this context, since
the new law will redefine who is "authorised" to do what. Another fake term is
"strong oversight arrangements", which as we have seen before is meaningless.
Leaked documents show that GCHQ is terrified of actual judicial oversight,
European oversight or public knowledge of its activities, embracing only limited
oversight from favourable intelligence officers and busy cabinet ministers who
receive only a report and will happily sign off on anything in secret.

May is quoted as saying that the government "will not be giving powers to go
through people’s browsing history", which is a blatant lie. They will know,
_without warrant_, precisely which gay adult sites you visited and when, with
the only limit that they don't know exactly which videos you watched.

May signs off on over 1,400 warrants per year, an average of at least 27 per
calendar week, and still insists that she spent "as long as necessary"
considering each one. If she spent ten minutes per warrant, that's four and a
half hours per week in addition to all her usual duties. If she spends less than
that, "as long as necessary" is an admittance that she signs everything GCHQ
puts under her nose; if she spends much longer, it's absurd for the Home
Secretary to squander so much of their time demanding to personally sign
warrants.

Remember also that one Home Secretary warrant was enough to sign off on Optic
Nerve, which targeted at least 1.8 million people, or Tempora, which has an
unlimited number of targets. Theresa May's 1,400 warrants are not necessarily
targeted warrants in the sense that the word "warrant" is normally used, but may
be a government waiver allowing unprecedented violation of basic rights and
nation-state level hacking of the kind the press normally condemns China for.

## Summary

The Snooper's Charter will have no effect on Facebook or Snapchat, but it will
completely outlaw iMessage, Facetime and Signal. It will weaken security in the
event that your service provider gets hacked. It will weaken the security of
WhatsApp and LINE, and will prevent companies from improving the security and
privacy of their app. It may force service providers to scan for and block all
PGP and OTR communications, at their own expense.

It will give police, intelligence agencies and other groups access to your
Internet history without a warrant. It will force ISPs to log your Internet
history, at their own expense, including privileged communications such as
lawyers and doctors, but will not protect you if that data is misused, leaked or
used for blackmail. It will almost certainly continue to allow warrants to be
signed by politicians instead of judges.

It will not prevent terrorists or criminals from using their own encrypted
communication.

## Conclusion

The message from the Tory government is clear: the power of the state to control
its own citizens is more important than the citizen's right to privacy.

This cannot be accepted. The people's right to privacy is a guaranteed right;
the government's desire to take control of the Internet is not.
