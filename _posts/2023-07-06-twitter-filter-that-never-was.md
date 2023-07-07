---
title: "The Twitter filter that never was"
category: comp
tags: twitter
description: "suggest_activity_tweet suggest_pyle_tweet suggest_who_to_follow"
license: CC BY
---

1. Table of Contents
{:toc}

A few years ago, a list of keywords began circulating on Twitter, with names
like `suggest_activity_tweet`, `suggest_pyle_tweet` and `suggest_who_to_follow`.
The idea was that these were internal Twitter identifiers for certain types of
tweet, and that by adding these keywords to the mute list, users could block
anything from advertising to followers' likes.

There's just one problem: they didn't work. The whole thing was superstition.

This article explores how the idea came to be, how it spread, why people
believed it, and how we know it never worked in the first place.

## The worsening of Twitter

From April 2014 to July 2019, web Twitter used an older design, which you can still see
with the browser extension Old Twitter Layout
([Firefox](https://addons.mozilla.org/en-US/firefox/addon/old-twitter-layout-2022/),
[Chrome](https://chrome.google.com/webstore/detail/old-twitter-layout-2023/jgejdcdoeeabklepnkdbglgccjpdgpmf)).
A trait of the old Twitter design was that HTML elements had meaningful class
names and attributes, allowing advanced users to customize their Twitter
experience with custom CSS or adblocking tools. For example, you could highlight
the tweets of people who follow you, or hide retweets entirely.

From February to March 2016, Twitter introduced the non-chronological
algorithmic timeline, which was unpopular with advanced users. By March 2017,
the algorithmic timeline was made worse by the inclusion of other users' Likes
[as evidenced here](https://twitter.com/AdParker/status/844162496546160640).
Likes were generally lower-quality than intentional retweets, especially
considering that many people used Likes very freely as read notifications or to
build engagement. The feature had previously been tested
[in 2014](https://mashable.com/archive/twitters-favorites-experiment), when
Likes were still called Favorites.

## The beginning of misinformation

On Japanese Twitter, divided from English-language Twitter by the language
barrier, people searched for a way to hide the tweets.

On 5 Mar 2017, Japanese user @strada_n
[suggested](https://twitter.com/strada_n/status/838306648653340674) adding a
keyword mute for the phrase "〜がいいねしました", "~ga iine shimashita",
Japanese for "liked". "It would be interesting to see if this works", says the
user. By 23 March, Japanese artist Nazuki makes
[this tweet](https://twitter.com/Arukas_nayu/status/844836565763293184),
expressing skepticism on the method since keyword mutes should only work on the
Tweet text itself.

On 6 May 2017, a correct way to hide tweets appears, seemingly independently by
multiple users, which uses custom CSS or adblocker rules to hide elements with
the HTML attribute `data-component-context="suggest_activity_tweet"`. On the
same day, similar methods using this attribute are tweeted in
[Japanese](https://twitter.com/tailtame/status/860748873953722368),
[French](https://twitter.com/minirop/status/860823912271273989) and
[English](https://twitter.com/metaly/status/860961261835624448), with
[another English tweet](https://twitter.com/adeyblue/status/862430176977850368)
using an adblock rule. A Japanese user would later
[extend the rule](https://twitter.com/guignol_ninja/status/885142351080865794)
to also block promoted tweets.

It's not until 8 June 2017 that the earlier mute method blows up on Japanese
Twitter. [This tweet](https://twitter.com/SpangleSpica/status/872825707381932036)
by Spica, which received over 20,000 retweets, notes that they haven't seen a
Like in their timeline since they muted "いいねしました", although it took a
little while for the effect to kick in. After this date, Japanese Twitter is
awash with tweets discussing the keyword mute. The method is widely shared,
despite tweets finding that
[it doesn't work](https://twitter.com/sharakudayo/status/876948487681613824).

On 12 June 2017,
[this article by user q7z](https://q7z.hatenablog.com/entry/2017/06/12/223433)
advises users how to apply the custom CSS in Google Chrome.
[Originally](https://web.archive.org/web/20170715234249/http://q7z.hatenablog.com/entry/2017/06/12/223433),
(Web Archive), the article makes no mention of the mute method, but it is soon
added in an addendum. The author believed that the mute method worked, but took
several hours to a day to take effect.

On 18 July 2017, Japanese user @mi1tu linked to q7z's article in
[this tweet](https://twitter.com/mi1tu/status/887225905482932224),
saying that while the mute method was ineffective, muting the term
`suggest_activity_tweet` did work. q7z updated the article to add it, but with
the disclaimer that they hadn't personally tested it. mi1tu's tweet received
over 4,000 retweets.

A few days later, Japanese Twitter was awash with the new method of muting
`suggest_activity_tweet`.

## Spread to English language

By the end of July 2017, muting `suggest_activity_tweet` began to spread to
English language Twitter via bilingual users, such as
[this tweet](https://twitter.com/minahomine/status/890652087217823744).
It's repeated by [this tweet](https://twitter.com/ohmaikii/status/891209742139351040)
by a Japanese translator and
[this one](https://twitter.com/melontoyo/status/891226238253244421)
by an illustrator, both of whom soon post that the method turns out to be
ineffective.

It's not until 13 September 2018 that the idea of muting `suggest_activity_tweet`
begins to spread through English-language Twitter in earnest. One of the first
is [this tweet](https://twitter.com/lexmaxine/status/1040299862351327232),
noting that it doesn't work, followed by
[this one](https://twitter.com/attackthemoon/status/1040313998720294912),
which claims that it does. The idea soon spreads throughout English-language
Twitter, while still circulating in other languages including Japanese, Spanish,
Arabic and Korean.

## Development

From there, users began circulating growing lists of keywords to mute. On 17
September 2018,
[this tweet](https://twitter.com/Mx_M_reads/status/1041633735945412610)
suggested muting `suggest_recycled_tweet_inline` and `suggest_pyle_tweet`.
The additing of a fourth muted word, `suggest_ranked_timeline_tweet`, according
to [this tweet](https://twitter.com/SuperMechaDad/status/1041681515359416320),
is credited with making a set which will even force the timeline to display in
chronological order.
[This tweet](https://twitter.com/Esquiring/status/1042039726562308096), on 18
September, lists eight and credits it with keeping the timeline chronological.

There is little consistency between different users' mute lists. The keywords
most likely were drawn from HTML attributes attached to various categories of
unwanted tweets. Most users appear to have accumulated their own set of keywords
by copying from other tweets they saw. Some entries begin with capital letters,
probably erroneously, while others omit underscores (e.g. `suggestpyletweet`)
or write "suggested" rather than "suggest".
[One such list](https://twitter.com/TrevorIsGood/status/1166699995707240448)
numbers 24 entries, of which 8 are probably erroneous variants.
[One list](https://twitter.com/gaydeviants/status/1156638268236161024) even
erronously mutes `filter: follows -filter:replies`, which is rather a Twitter
search intended to show chronological timeline, and not intended to be muted.

By June 2019, mentions of the legitimate CSS or adblock method have given way to
these lists of collected mute keywords.

## New Twitter

In July 2019, the new web Twitter design launched, which as of July 2023 is the
current design.

The new Twitter made a major change, which is to eliminate all of the useful
attributes from the HTML tags. The new HTML is horribly inefficient, with some
elements possessing ten or so class names, none of which are descriptive. A
single sample tweet within a timeline, consisting of 186 characters, uses 13,491
bytes of HTML text, more than 72 times as much. A page for a single tweet
consists of a full quarter of a megabyte.

Notably, this change means the keywords circulating in mute lists no longer
appeared anywhere in web Twitter's front end. This did not prevent people from
continuing to circulate the existing keyword lists, nor did it discourage belief
in their efficacy. However, it did prevent new entries from being added to the
list, since they no longer had a source of clearly defined HTML attributes to
draw from.

For example, on 1 August 2019, [this article](https://www.osintcurio.us/2019/08/01/muting-the-twitter-algorithm-and-using-basic-search-operators-for-better-osint-research/)
presented the mute list strategy, along with 15 keywords, all of which appear to
be correctly spelled and drawn from Twitter's HTML attributes. The article
presents them as a solution to new Twitter design, following a complaint on the
matter by security expert @thegrugq.

The mute lists continued to be shared, even by highly technical users who ought
to have been more skeptical. On 3 January 2020, @IanColdwater posted 
[twittermute.txt](https://gist.github.com/IanColdwater/88b3341a7c4c0cf71c73ac56f9bd36ec)
to GitHub, a list of 21 muted keywords including three misspelled with missing
underscores. It received 1,892 Stars at current count, and was lauded with
praise in the comments, including Javascript snippets to automatically add the
entries to the mutelist.
Even the [Hacker News thread](https://news.ycombinator.com/item?id=22141903)
on the list was limited in its skepticism.

As of July 2023, mute lists are still being distributed on Twitter. In many
cases, the list is truncated to a list of 12 entries for a total of 277
characters, constrained by the tweet limit of 280 characters.

## Why did anyone think it worked?

There's a [famous gaming anecdote](https://gamersdecrypted.com/superstitions/)
about the beta of _Dungeons & Dragons Online_. Due to an oversight, it was
possible to use the Diplomacy skill on treasure chests. Players began to believe
that doing so would increase the treasure, and refused to take part in raids
without a Diplomacy master in the party. They continued to believe in it even
after the developers explained that it didn't work. It was complete
superstition.

A superstition consists of a set of actions which are which is supposed to
attain a desired benefit. Proof of efficacy is not necessary, as long as there
is no immediate disproof. A superstition is validated by the number of people
who appear to believe it. Once it becomes established, contrary evidence is
rationalized away for fear of losing the benefit.

Some users certainly shared the mute list without checking if it actually
worked. Other people are saying it, after all, and those people had no
particular motive to lie.

Of the users who did try it, surely some did not report when it failed, meaning
users had poor feedback on the system's lack of efficacy. Failure to report
negative outcomes is even a problem in mainstream science.

Some users even reported that it seemed to work, but because they did not apply
the scientific method, they were unable to prove that the mute list, rather than
other associated or unrelated factors, were removing Twitter junk. Possible
conflating factors might include:

- Suggested tweets were shown to on first visit after a time, to allow users to
  catch up on what they missed. Fewer promoted tweets were shown later.
  Refreshing the page after editing the mute list would therefore trigger the
  reduction. In fact, the effect would be triggered by the refresh, even if you
  didn't edit the mute list.
- Many users would also switch to chronological Latest Tweets timeline as part
  of the process. This timeline may have been shown less junk content.
- A/B testing may cause users to be shown more ads at first, and fewer ads later
  on.
- Over the long term, the suggested tweets feature may have been reduced for all
  users following user feedback or analytics.
- The placebo effect may cause users to assume the mute list was doing
  something, when it had no effect. An excess of optimism could have biased
  their perception.
- Users may apply additional methods to block junk at the same time, and
  conflate the efficacy of those other approaches. One user altered their uBlock
  Origin settings at the same time as the mute list, and was later unable to
  replicate the effect.
- Adblock lists may have automatically updated to block Twitter junk. Users of
  adblock may have seen long-term reductions in suggested tweets and falsely
  attributed it to mute lists.

Some users noticed that it didn't work, but invented rationalizations to explain
why. Actual theories among mute list users included:

- You need to wait a few hours to a day for it to take effect. (By that point,
  you have already shared the mutelist and forgotten about it, so the idea
  spreads.)
- It used to work, but Twitter changed the keywords. As soon as someone
  discovers the new keywords, you need to need to add them to the mute list.
- It works, but unreliably. It only works sometimes, or only for certain people.
- It does work, but it only reduces the junk tweets, rather than eliminates
  them.
- It works on Japanese language users, but the feature may not have been rolled
  out yet for English language users.
- It works, but you have to perform additional steps, such as refreshing the
  page, force-refreshing the page, or switching to Latest Tweets timeline.
- Twitter Support says it doesn't work, but they're probably lying to keep the
  feature a secret because they don't want people using it.
- It used to work, but has recently stopped working.

## Conclusion

The two biggest factors, almost certainly, were that refreshing the page and
switching to the Latest Tweets timeline were effective in clearing junk in the
short term. Users who edited their mute list would often perform both actions,
allowing the illusion that the mute list was the active ingredient.

At no point did anyone prove that keyword muting worked, or demonstrate a
provable mechanic by which it would work. The keywords did work as adblock
targets, but only until the July 2019 redesign. Using them as keyword mutes
never had any effect because mutes only ever applied to tweet text. Yet, as of
writing, people are not only still sharing Twitter keyword mute lists, but also
insisting that they've observed it working.
