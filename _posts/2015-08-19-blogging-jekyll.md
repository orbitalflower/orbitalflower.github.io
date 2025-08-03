---
title: "Advantages of blogging with Jekyll"
category: comp
tags: jekyll
redirect_from:
- 20150819-blogging-with-jekyll.html
description: 
license: CC BY
---

As a content management system for websites and blogs, Jekyll has its advantages
and drawbacks. I thought I'd share my experiences here.

In comparison to blogging engines like Wordpress, Jekyll users write posts
locally and compile these into flat files. In the olden days we would have
uploaded these to a server with FTP, but nowadays something like rsync or git is
more secure.

Right away there are several usability hurdles that will stump non-technical
users:

* Jekyll comes with no default theme, so you have to find one or build your own
* Users edit posts by writing a markdown format file which must have a specific
filename: the correct date in international format, followed by the post slug,
separated by dashes.
* Users must manually include "front matter" or metadata in their posts, which
at minimum is only the title, but it's easy to forget the syntax
* You need to install ruby, jekyll, and jekyll's dependencies to build pages
yourself, and can only update the site from a device that has these installed.
You don't have to do this if you use Github's page hosting, but then you need to
learn git
* Flat files mean no dynamic features like comments, search, page counter, or
automatic scheduled posts

But if you can deal with all of these issues, then what you have is an excellent
system with many advantages:

* Highly efficient and cheap to run, since the server doesn't have to spend CPU
time dynamically generating pages, and you can sometimes find non-dynamic
hosting cheaper
* Laugh heartily every time a new security vulnerability is discovered in
Wordpress; your flat files are immune
* No web-facing login over insecure HTTP; all updates are ideally made over
secure channels
* Highly customisable; pages can contain arbitary metadata, which themes have
access to, and the theme templating system is flexible
* Easily backed up and ported to any other web server; even if your entire
server is lost you can rebuild the entire site from the local copy
* Drafts can be edited offline in any text editor, so you don't need internet
access to write posts or save drafts

Compared to the old-fashioned way of writing a webpage in raw HTML like it's the
1990s, Jekyll is still advantageous. You gain the benefit of a templating system
and Markdown saves you writing a lot of markup tags manually.

You can run a Jekyll-based site for free, without installing Jekyll locally,
using Github Pages.

Github Pages it will also let you serve pages over HTTPS, which is very
good for security; even if your site has nothing but text, HTTPS ensures it
won't be interfered with in transit (e.g. a malicious wifi hotspot, DNS
hijacker, proxy service or greedy ISP might inject malware, adware or tracking
cookies into the HTTP stream, all very real threats in 2015).
