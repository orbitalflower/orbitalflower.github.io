---
title: "Intel's 5 security tips are spot-on"
category: comp
tags: security
redirect_from:
- 20150329-intels-5-security-tips.html
description: 
license: CC BY
---

Intel's [#5habits](https://digitalsecurity.intel.com/5habits/)
list ought to be required reading for all Internet users today.
{:.lead}

## #1: Think before you click

I'd extend this rule: __don't click links in e-mail (almost) ever__.

E-mail is inherently untrustworthy. Unlike modern web services, e-mail has no
central user database allow users to authenticate the sender of a message. 
Without an additional system like
[PGP signatures](https://orbitalflower.github.io/20150219-why-pgp-will-never-be-mainstream.html),
you have no way to prove that your e-mail came from the person it claims.

As a result, you can't trust links in e-mail even from sources you know,
since you can't be sure it's really them. Once a single link leads you to
a site controlled by an attacker, they can deploy all manner of exploits
from malware infection to stealing passwords.

Intel says 95% of all hacks were caused by clicking bad links, and I'd
believe it. __Clicking links in e-mail is how you get hacked.__ Don't
click links.

## #2: Use HTTPS

HTTPS encrypts data between the user and the server to prevent anyone else
from intercepting it to read or modify the content.
Most people thought regular HTTP was secure enough, since you can't snoop on
internet traffic without somehow directly wiretapping the internet backbone,
and you'd need the authority and resources of a nation state to do that.

Then, in 2013, it was revealed that actually, several nation states
[are doing that](https://en.wikipedia.org/wiki/Tailored_Access_Operations).

> You could read anyone's email in the world, anybody you've got an email
> address for. Any website: You can watch traffic to and from it. Any
> computer that an individual sits at: You can watch it.
>
> --- Edward Snowden, on [XKeyscore](https://en.wikipedia.org/wiki/XKeyscore)

Unsurprisingly, demand for HTTPS has skyrocketed.

HTTPS is an extremely good idea, since it's not only your government reading
your web traffic. Your data could be intercepted over insecured public wi-fi,
or a
[vulnerability in your router](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Setup#Vulnerabilities),
or a [weakness in phone internet cryptography](https://en.wikipedia.org/wiki/Mobile_security#Attacks_based_on_the_GSM_networks),
or a suspicious routing glitch
[detouring your data through foreign countries](http://arstechnica.com/security/2015/03/mysterious-snafu-hijacks-uk-nukes-makers-traffic-through-ukraine/),
or by a [DNS spoofed website](https://en.wikipedia.org/wiki/DNS_spoofing#Prevention_and_mitigation),
or an untrustworthy VPN or Tor exit node, or a
[page-modifying proxy](https://en.wikipedia.org/wiki/Captive_portal)
on your school or workplace. Secure communications are more important than ever
in the era of wireless internet.

Intel is quite right to recommend HTTPS. As of 2015, you should no longer
download software from websites unless they use HTTPS, nor should you
allow Flash content or trust websites with personal information, passwords or
logins unless they use HTTPS.

I wholeheartedly agree with Intel suggests the HTTPS-enabling browser extension
[HTTPS Everywhere](https://www.eff.org/https-everywhere), but bear in mind
that it doesn't enable HTTPS on _all_ sites, it only enforces it on for the
increasing number of sites which already support HTTPS.

## #3: Manage passwords

This.

Humans are [bad at generating strong passwords](https://orbitalflower.github.io/20150328-stop-numb3r1ng-up-passwords.html)
and bad at remembering many passwords, so you use the same password everywhere,
and when one site gets hacked they all get hacked.

Until the day we move to
[passwordless login](https://orbitalflower.github.io/20150117-whatever-happened-to-openid.html),
the best solution is to have password manager software generate and remember
a strong password for every website.

I suggest memorizing a strong password to your main e-mail account, then using
a password manager to remember everything else. It is vital to have access to
your e-mail account to receive password reset e-mails in the event that you
lose access to your password manager (e.g. hard disk failure or theft).

## #4: Two-factor authentication

Two-factor is the greatest invention in authentication since OpenID failed
to catch on.

You want two-factor enabled for at least your main e-mail account. Even
if someone does get your password (which can happen via weak passwords,
password re-use, phishing, etc) they can't access your account without also
stealing your phone or at least intercepting your text messages to steal
the two-factor SMS code, which makes it significantly harder.

A corollary is that you also want to enable encryption on your phone with
a strong lock screen password, in case your phone is stolen too. Walking
around with your entire digital life in your pocket without encrypting it
is _insane_.

Always generate backup codes in case your phone or authentication device
fails or is stolen. It's equally important that your security measures
don't lock yourself out of your own account.

## #5: VPN

A VPN is often unnecessary, and could give you a false sense of security:
it won't protact against malware or stop your accounts being hacked. It
won't make you immune to advanced surveillance since it just changes the
endpoint.

Where you do want a VPN is any time you need to use the internet but can't
trust the connection you're using: usually public wifi, or potentially
mobile data. Many apps send private data unencrypted, even when running
in the background. If you trust the Internet with this data, but not the
access point you're using, enable a VPN.

Don't use free VPNs; they may be poor quality or inject advertising into
webpages, which in turn could include malware.

HTTPS-based sites are better than a VPN, since they encrypt all the way to
the server and are safe even over an untrustworthy connection. However, other
apps on your phone can send and receive data over the connection, so even
when browsing a HTTPS site over unsecured wifi the rest of your computer
could be at risk. The safest solution is to avoid public wifi.

## Links

* [Intel #5habits](https://digitalsecurity.intel.com/5habits/)
* [HTTPS Everywhere](https://www.eff.org/https-everywhere)
