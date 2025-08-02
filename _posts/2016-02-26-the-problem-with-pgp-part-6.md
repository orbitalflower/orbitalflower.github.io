---
title: "The problem with PGP, part 6"
category: opinion
tags: pgp
redirect_from:
- 20160226-the-problem-with-pgp-part-6.html
description: 
license: CC BY
---

> To the person who sent me a PGP message via Tumblr. I appreciate your
> enthusiasm, but you've overestimated my excitement for PGP. Email me.
>
> --- [@thegrugq](https://twitter.com/thegrugq/status/702563720254267392),
> 2016-02-24

The Grugq is a popular infosec expert who publishes a PGP key online for people
to contact him, and even he can't be bothered to decode PGP messages by hand.

Presumably, he can only bear to use PGP within an email client preconfigured to
reduce the effort to nearly zero. And this is still too much work for the ACLU's
Christopher Soghoian, who has declared that he's "taking a PGP break", or
cryptographer Nadim Kobeissi who considers it [too much trouble for trivial
use](https://twitter.com/kaepora/status/699829540063993856).

And these are all highly technical people. How would the average person handle
PGP?

> @thegrugq Now he’ll encrypt it to himself and then send it to you. I get that
> one a lot at work.
>
> --- [@makehacklearn](https://twitter.com/makehacklearn/status/702694009139888128)

PGP is easy for a novice to use incorrectly. The user can fail to send or
receive, either because it's too hard to use and they give up, or they use it
incorrectly without realising. They can fail to ensure correct security, such as
failing to correctly validate keys.

This in turn means that even an expert cannot be certain that his communications
are secure, since they cannot be sure that their conversation partner's
security is solid.

I hesitate to say that "PGP is dead", because software can come back to life
when technology or circumstances make it feasible again. But PGP is not
mainstream ready, and will not unless it becomes standard and automatic, and a
system is developed to validate keys.

Even so, there is the problem that PGP inherently requires the user to take
responsibility for their own key. Most communications systems only require the
user to remember their password, and even that can typically be reset as long as
the user has access to their email.

That evolves two situations. One way the user is locked out of his own email if
he loses the key. Way two, the user is not responsible for his own key, which
essentially means trusting the email provider to hold the key. At that stage
there's no real difference from using STARTTLS to encrypt between servers, which
is what Google is doing now.

If your mail is safe from Google, it's also "safe" from Google's spam filter. It
could become plausible for spammers to not only share databases of email
addresses, but also the public keys associated with those addresses, thus
circumventing spam filters.

For reasons like this it seems unlikely that major mail providers will enable
PGP for their users as standard, and therefore it will not catch on. Current
users don't see the benefit of such a system and won't expend any effort to
upgrade to it.

Therefore while everyone already has email, PGP has no reason to become popular.
If tech leaders can't handle it, the general audience has no chance.

## Previously

* [The problem with PGP, part 5](20151103-the-problem-with-pgp-part-5.html)
