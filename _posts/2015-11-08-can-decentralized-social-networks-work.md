---
title: "Can decentralized social networks work?"
category: opinion
tags: 
redirect_from:
- 20151108-can-decentralized-social-networks-work.html
description: 
license: CC BY
updated: 2025-08-01
---

> I'm in the superalpha of Google Minus, the social network for narcissists.
> It's just me. Check it out.
>
> --- Tycho, [The New Shit](https://www.penny-arcade.com/comic/2011/07/25/the-new-shit), Penny Arcade

Between the failure of Google Plus, ongoing controversy of Facebook's policies
and the complete irrelevance of nearly anything else, many users are hoping for
a social network that both respects their rights and offers the features they
expect.

But easily the number one problem with social networking today is that Facebook
has such a mass of users, it has a kind of _user gravity_ that prevents any new
site from pulling away its users.

Ello and Tsu.co have grown in popularity, but only by making considerable
promises. Ello pledges never to use advertising or sell user data, which could
pose financial challenges if the site gets big. Tsu.co instead offers users a
split of advertising revenue, with pyramid scheme style incentives for inviting
new users.

But even this isn't enough to steal Facebook's user base. Sites are promising to
treat you better than Facebook, or even paying you to recruit users, and they
still can't compete.

## The origin of social networks

LiveJournal was one of the earliest popular examples of what we would today
recognise as a social network.

Blogs, or "weblogs" as they were originally known, existed before LiveJournal,
but were usually written manually in HTML on the user's PC and uploaded to their
own web server by FTP. The novelty of LiveJournal was that it offered an online
content management system, which opened up blogging to many non-technical users
for the first time.

What made this into a social network was actually an emergent property of a
second feature, namely locked or friends-only posts. To solve the problem of
identifying which readers were allowed to see locked posts, LiveJournal required
them to create an account and log in, creating an identity in their system that
a user can share a closed blog entry with.

And because users often wanted to share all posts with a selected set of users,
LiveJournal added the friends list feature, along with the ability to request
entry to another user's friends list.

LiveJournal further added a convenient friends page where a user could read a
sorted list of all their friends' posts, including locked friends-only posts, in
reverse chronological order. And so the design of every major social network for
the next fifteen years was established.

## Social networks now

Facebook is essentially nothing more than a hi-tech clone of LiveJournal. Its
only major differentiating feature is its real name policy.

On LiveJournal, as was the style in the early 2000s, users took on aliases and
joined groups based on shared interests instead of existing real-world social
groups. Sharing one's real name online was uncommon at the time, especially
among young people who were warned against sharing personal details online for
their own safety.

Facebook changed that. It came from a college user background where
geographically close people could expect to interact in real life, and use their
real name. Its real name policy helped the site gain mainstream popularity as
people were able to find real-world friends in the system and map out their
real-world relationship patterns.

A big difference can be seen between this and sites where real name use is
uncommon and even discouraged. Tumblr uses the LiveJournal reverse chronological
friends list pattern, but users tend to follow others based on interest and
quality of content, especially high quality reshared content. Users funnel
content to each other based on personal preference and self-expression,
irrespective of their real-world identity.

In fact, users often express concern about their real world social groups
discovering their Tumblr identity, and intentionally avoid using the site to
model real-world social connections - the exact opposite of Facebook.

This is partly because Tumblr lacks LiveJournal style friends-only posts, so the
only practical way for users to share private thoughts without real-world social
connections reading them is to post openly under an alias that nobody will think
to look for.

Conversely, Facebook allows friends-only posts, but forbids the use of a
nickname or alias.

## Problems

Facebook's real name policy [has been
controversial](https://orbitalflower.github.io/20150226-facebook-real-name-policy-must-end.html),
especially for minority groups who are discriminated against and have good
reason not to reveal their birth name: transgender people, abuse victims, ethnic
minorities, children, and human rights activists in less free countries, among
others.

There are also privacy issues, such as that Facebook can track you across the
Web on any site that includes a Facebook "Like" button. Google has similar
powers, but backed down on its own real name policy a while ago.

On any such site, you're limited to whatever rules the network wants to impose
and whatever data they want to collect on your social graph. A growing number of
people are disgruntled with Facebook, but still want the ability to share with
friends.

## Decentralized social networks

A simple social networking solution is for a group of people to start their own
blogs, either using an easy service like Wordpress.com or their own self-hosted
solution over which they have full control. They then subscribe to each other's
RSS feeds using a feed reader to create their own timeline.

This solves most of the privacy and control issues of today's social networks,
but at the cost of several features:

* You can't make friends-only posts, at least, not easily
* It's hard to do any sort of non-public content over RSS
* RSS is not real-time, and people today expect up-to-the-minute updates
* Each blog provider has its own login for comments; if anonymous comments are
allowed, it can allow commenter impersonation and spam

There is some talk of a social network using XMPP, a real-time instant message
protocol. An impromptu XMPP social network would be quite possible; in fact,
similar systems date back to the eighties with IRC.

There are also free software alternatives like Diaspora, intentionally created
as an open Facebook replacement, and GNU social (aka StatusNet), a free Twitter
clone, among numerous other less well known open source services. Many such free
services are federated, meaning that accounts on different servers can
communicate with each other, even if you run your own server.

## The drawback to federation

Unfortunately, decentralized services suffer from a flaw which should be obvious
to anyone whose e-mail account has ever received spam.

Each provider can only validate its own users, and has to trust that any server
sending it messages is correctly validating its own users. Since anyone can run
an e-mail server or or GNU social server, all server operators have the
challenge of blocking spam from users it can neither directly observe nor
control.

The result is that while open networks are good for freedom, they're also open
to people willing to misuse that freedom.

Still, such open systems are generally not as completely decentralized as, say,
USENET was. On GNU social, your account is tied to a server, and the server
operator can delete old access. On USENET, all messages join a communal pool
which is replicated across all participating servers, and so any messages
previously sent stay in the system. That, of course, made it even more difficult
to block spam accounts.

With modern free software networks, you're still at the mercy of the server
operator, and frequently reliant on an unpaid volunteer to keep the server
running and secure.

This wasn't such an issue with IRC where the server held no important long-term
data and the admin could point the domain name at another server in the network
without causing a problem, but a social network holds years of personal data and
is expected to keep that available and secure.

## The people problem

The biggest problem, in the end, is that despite its failings, Facebook is where
all the people are, and they won't move.

And since they're encouraged to share their real names, real phone numbers and
even real geolocation data, the users who are there have an easier time finding
each other, which compounds the impression that Facebook is where all the people
are.

Facebook has _user gravity_, a density of people that attracts other people
since they want to be near their friends. It pulls in new users more strongly
than any other social network, so that for many it is their only social network,
or the only social network that all their friends use.

For the same reason, it's difficult for someone who's in it to leave. You won't
go to Ello even if you like their privacy policy better, because none of your
friends are on Ello and you can't convince them to all move because, in turn,
all _their_ friends and family are still on Facebook. The social graph is almost
like a chain gang that binds people to one site.

That pull, more than the quality of the software or servers, is why it will be
very difficult for any social network to overturn an established system like
Facebook.

The main reason why Facebook has 1.4 billion more users than Diaspora is that
Facebook has 1.4 billion more users than Diaspora.

**Update** (August 2025): Tsu.co re-named itself to "display" in 2021, and shut
down in June 2025. Ello shut down in July 2023. Mastodon has shown that
decentralized social networks can work, although with their own set of
challenges, while Bluesky is currently thriving, although it is still highly
centralized.
