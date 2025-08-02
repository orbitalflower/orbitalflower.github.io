---
title: "How SourceForge started spreading adware"
category: opinion
tags: 
redirect_from:
- 20150529-how-sourceforge-started-spreading-adware.html
description: 
license: CC BY
---

SourceForge used to be the top site for open source project hosting and
downloads, but the site's recent decision to inject adware into downloads has
been [the last straw](https://helb.github.io/goodbye-sourceforge/) for what has
become an increasingly obsolete and problematic service.

## November 2011: Noble goals

In November 2011, SourceForge created the [Sourceforge Open Source Mirror
System](http://sourceforge.net/mirror), a feature to offer downloads of open
source projects that didn't have their project pages at SourceForge. The initial
goal was to make SourceForge a more ethical competitor to download sites that
embedded toolbars and adware:

> Yes, there are a few other places that list free software products, but a
> number of them offer downloads that include unwanted addons like browser
> toolbars, install wrappers, and various other malware. This, in turn,
> undermines the trust and openness that should be at the core of free software,
> and that hurts everyone that cares about Open Source. We want to provide a
> place where you can trust that you're only getting the exact product that was
> provided by the original packager.
>
> --- [The SourceForge Open Source Mirror Directory, 5 Jan 2012](https://web.archive.org/web/20120105054330/http://sourceforge.net/mirror)

Minor changes by the following [5 January](https://web.archive.org/web/20120105054330/http://sourceforge.net/mirror)
renamed the project from Mirror System to Mirror Directory and promoted it as
free publicity for open source authors:

> We’re putting your software in front of more than 40 million additional
> potential users a month.

The accounts sf-editor1, sf-editor2 and sf-editor3 were created on November 3
2011 for the purpose of maintaining the mirror project pages.

## Summer 2013: SourceForge embraces adware

Between [2 May 2013](https://web.archive.org/web/20130502103606/http://sourceforge.net/mirror/)
and [12 Sept 2013](https://web.archive.org/web/20130912103533/http://sourceforge.net/mirror),
SourceForge made a subtle but significant change to its page. Removals are shown
below as strikeout, additions in bold:

> Yes, there are a few other places that list free software products, but a
> number of them offer downloads that include <s>unwanted addons like browser
> toolbars, install wrappers, and various other</s> malware. This, in turn,
> undermines the trust and openness that should be at the core of free software,
> and that  hurts everyone that cares about Open Source. We want to provide a
> place where you can trust that you're only getting the exact product that was
> provided by the original <s>packager</s> __project__.

The change in message is significant:

* SourceForge deletes its assertion that adware is a form of malware,
effectively abandoning its promises not to include adware in downloads
* SourceForge abandons its promise to provide original unmodified packages,
allowing it to use install wrappers or modified versions including adware

Between [3 Dec 2013](https://web.archive.org/web/20140210032935/http://sourceforge.net/mirror/)
and [10 Feb 2014](https://web.archive.org/web/20140210032935/http://sourceforge.net/mirror/),
SourceForge cut the paragraph altogether. It also proudly increased its user
count statistic from 40 million to 42 million.

## 2015: SourceForge captures abandoned projects

Between [21 Mar 2015](https://web.archive.org/web/20150321051042/http://sourceforge.net/mirror/)
and [22 Apr 2015](https://web.archive.org/web/20150422025455/http://sourceforge.net/mirror/),
the SourceForge Open Source Mirror Directory expanded to include projects which
were "abandoned": projects which used to be on SourceForge, but left for one
reason or another.

One such project was VLC media player, which [left around April
2013](https://blog.l0cal.com/2013/05/02/rethinking-vlc-mirrors-infrastructure/)
over issues like misleading advertising on download pages, where SourceForge
displayed ads for scam sites or malware disguised as download links. While it's
common for sites like SourceForge to outsource to ad networks like AdSense that
they have no control over, the "fake download link" issue has been a serious
problem with SourceForge for years and the lucrative click-through ratio and
high payout on such ads encourages the site to turn a blind eye.

The official reason for reclaiming abandoned projects is to ensure visitors to
SourceForge always have the latest version. While this is benefifical to
visitors, it also ensures users continue to flow to the old SourceForge URL
which now has scam advertising and adware installers, served over
[insecure HTTP](https://orbitalflower.github.io/20150514-why-im-happy-http-is-going-away.html)
even though SourceForge has a working SSL server. And former maintainers
complain of being locked out of their old project.

An earlier edit that year reassures users that SourceForge consults the
original project's website to ensure the correct license is attributed to the
project. It appears that SourceForge was already respecting this requirement,
but between January and March 2015 felt the need to reassure users that it was
acting in accordance with the open source licenses.

Another small change is the URL structure of "mirror" projects, which move from
`/projects/projectname.mirror/` to `/mirrors/projectname/`, while abandoned
projects remain the same as their old URLs.

The mirror project directory list page is also gone, but the project lists on
the sf-editor1 account show some of the reclaimed abandoned projects which can
be identified by their URL: Apache Allura, Audacity, CDex, GIMP for Windows,
Jokosher, LinuxLive USB Creator, Serna Free, TigerVNC, VLC media player, WarMUX,
an old version of ytdownloader, and synergy. In some cases, but not all,
SourceForge has courteously placed a link at the top notifying users of the
project's new site after it left SourceForge.
