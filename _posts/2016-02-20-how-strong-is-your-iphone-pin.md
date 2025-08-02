---
title: "How strong is your iPhone PIN?"
category: opinion
tags: security
redirect_from:
- 20160220-how-strong-is-your-iphone-pin.html
description: 
license: CC BY
---

> The passcode is entangled with the device’s UID, so brute-force attempts must
> be performed on the device under attack... The iteration count is calibrated
> so that one attempt takes approximately 80 milliseconds.
>
> --- [iOS Security
> Guide](https://www.apple.com/business/docs/iOS_Security_Guide.pdf) (PDF), Apple

In [an article for the
Intercept](https://theintercept.com/2016/02/18/passcodes-that-can-defeat-fbi-ios-backdoor/),
Micah Lee notes that even with unlimited retries, an iPhone still resists a brute
force even if its PIN is only 11 digits numeric.

## iPhone security

The iPhone 5S and all variants of the iPhone 6 encrypt files with a combination
of a fixed hardware ID that cannot be extracted from the device, and the user's
PIN code.

This excellent security feature makes it impossible to either pull the key
directly from memory, or to brute force the device storage with a faster
computer.

Even if the FBI successfully forces Apple to remove the PIN retry limit, they're
still hard-limited by the speed of the iPhone hardware, which Apple gives as
about 80 milliseconds per attempt, or 12.5 attempts per second.

Compare this to something like Hashcat on a high spec PC, which can brute-force
many password hashes at a rate of billions per second.

## How strong is an iPhone PIN?

Firstly, iOS 9 enforces a limit of one PIN attempt per hour after the first nine
failed attempts, and optionally erases after ten. Nobody is dealing with the
FBI's 12.5 attempts per second scenario (yet, anyway).

Even with a special PIN-entering machine working around the clock, it would take
416 days and 16 hours to try every possible 4-digit pin, and over 114 years to
try every 6-digit pin.

With auto-erase, the chance is only one in a thousand to break a 4-digit PIN. If
your number is predictable (1234, 0000, 2580) it's highly likely to be broken.

## The "FBI wins" scenario

But suppose Apple really is forced to hack an iPhone to let it break at the full
rate of 12.5/sec, or some public exploit becomes available one day that has the
same effect.

A 4-digit PIN is broken within 14 minutes. A 6-digit is broken within 22 hours.

By 10-digit, we're at a much less assailable value of over 25 years. By
11-digit, 253 years. The FBI's backdoor would be useless, except of course as a
legal precedent to force Apple to roll out considerably more effective backdoors
as standard in the next generation of iPhones.

Even stronger, however, is a password consisting of three randomly selected
words, such as from the Diceware word list. This has the advantage of being
easier to remember than eleven digits. Even stronger is eight random
alphanumeric characters, where we start to exceed 2<sup>40</sup>.

## Anything but an iPhone

The current iPhone's hard-limit of 12.5 attempts per second will not apply to
other devices. You will memorize huge passwords to be secure, or hope nobody
serious tries to hack you, or switch to iPhone.
