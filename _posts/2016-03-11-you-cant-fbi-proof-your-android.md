---
title: "You can't FBI-proof your Android"
category: opinion
tags: security
redirect_from:
- 20160311-you-cant-fbi-proof-your-android.html
description: 
license: CC BY
---

An article was posted today titled [How to FBI-proof your
Android](https://the-parallax.com/2016/03/11/fbi-proof-android/) actually fails
to describe how to FBI-proof your Android.

The article describes a six-character alphanumeric passcode as "hard-to-crack"
security. This [would be true on new
iPhones](https://orbitalflower.github.io/2016-02-20-how-strong-is-your-iphone-pin.md)
where the hardware imposes a rate limit of around 80ms per attempt or 12.5
passwords per second.

It's entirely incorrect to assume Android has the same protection.

## iOS Security

The iPhone actually has multiple defensive layers that Android doesn't.

1. The iPhone can be set to erase after 10 failed retries.
2. Even if the user disables this, the software limits retries to one per hour,
equal to 2<sup>13.10</sup> attempts per year. A four-digit PIN has a search
space of 2<sup>13.29</sup>.
3. You can't replace the software to circumvent this limit because the security
hardware prevents jailbreaking.
4. Even if a jailbreak or exploit is discovered or Apple is forced to engineer
one, the hardware limits you to about 12.5 attempts per second or
2<sup>28.55</sup> per year. A 6-char alphanumeric PIN has a space of
2<sup>31.02</sup> and it would take over five and a half years to try every
possible combination.
5. You can't replace the security hardware because it's also necessary to
decrypt the files. Nor can you pull the keys from memory, or decrypt the storage
with faster hardware.

## Android is not FBI-proof

Android has none of these features. It has reasonable security against average
attackers, but it's not FBI-proof.

It's generally possible to jailbreak Android phones, to the extent that an
estimated 50 million Android users run the third party OS CyanogenMod. Such a
custom OS would easily circumvent any software limit, allowing unlimited PIN
retries at maximum device speed.

But we aren't limited to the 12.5 attempts per second that the iPhone imposes,
because there's no custom hardware required. We can even dump the entire
contents of storage to a more powerful computer and crack it from there,
allowing attacks in the range of a million per second or higher. At that rate, a
six digit alphanumeric PIN could be broken within a day.

A cold boot attack, which has been achieved before on Android could do this even
more quickly, simply by pulling the keys from memory.

The FBI are asking Apple for help breaking into an iPhone. They aren't asking
Google for help breaking into Android because they don't have to.
