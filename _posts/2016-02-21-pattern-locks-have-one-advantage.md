---
title: "Pattern locks have one advantage"
category: opinion
tags: security
redirect_from:
- 20160221-pattern-locks-have-one-advantage.html
description: 
license: CC BY
---

Smartphone "pattern" style lock screen suck. They're innovative, but ultimately
an inferior variant of the numeric PIN lock screen in almost every way.

The pattern lock is essentially just a numeric PIN where the numbers must form
a continuous line. Each digit must be adjacent to the previous digit, double
digits are impossible, and there is no zero. This considerably limits the number
of permutations.

For example, on a 4-digit line, only 952 of 10,000 possible numeric PINs form
valid pattern locks, and for 6-digits only 22,272 of 1 million possible PINs are
valid pattern locks.

Furthermore, there are general human biases that make it more predictable.
People probably start near the top left, and incorporate a lot of movement or
use simple patterns like letters. For example, a Z-pattern or spiral are
probably more common than the equally valid "898969".

Worse, the smudge left on the screen by a swipe is greater than that left by a
tap, and provides greater information about the order in which the digits were
hit.

All this said, pattern locks have one advantage over numeric PIN: __you can't
enter four of the same number__. It's impossible to enter a code like 1111 or
0000, which are usually the first guessed.

This isn't enough to make it a secure choice, but it does at least protect users
from making the most common PIN mistake.
