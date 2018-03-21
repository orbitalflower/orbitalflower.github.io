---
title: "Blogging with Jekyll"
categories: comp web
redirect-from: /20150819-blogging-with-jekyll.html
---

Jekyll is a flat-files based content management system suitable for building
websites and blogs.

Compared to something like Wordpress, a web-based blog content management system
which as of 2018 [runs on over
30%](https://w3techs.com/technologies/overview/content_management/all) of the
top 10 million websites, Jekyll requires more technical skill. Users write
webpages in Markdown or HTML, which is then compiled into flat HTML.

## Advantages of Jekyll

* __Security__: You do not need to maintain security updates, like you would on
  a Wordpress installation. The number of insecure outdated installations of
  Wordpress, and other CMS software is terrifying, not to mention vulnerable
  Wordpress plugins. If you host on Github Pages, you don't even need to
  maintain the server itself.
* __Easy backup__: There is no database to speak of. If you can copy the files,
  you can create a backup of your site. If your server goes down, you can
  rebuild the entire site from your local copy.
* __Highly flexible__: You can easily add custom meta tags. The theme templating
  system is highly flexible.
* __Edit offline__: You can edit offline in your text editor of choice. You do
  not have to deal with overly-clever Javascript based editing windows, or
  losing drafts, or finding internet access to write. You can write in anything
  that creates plain text files.
* __Efficient__: There's no server-side code like PHP, meaning that the site
  runs quickly and more cheaply, and can be hosted anywhere that hosts files
  rather than requiring PHP hosting.
* __Github Pages support__: You can host your site for free on
  [Github Pages](https://pages.github.com/). It even supports HTTPS and custom
  domains, even both at the same time, which as of 2018 is superior to many paid
  web hosts and services.
* __No insecure login__: As of 2018, many self-hosted blogs still don't use
  HTTPS, meaning that their login page is handled over raw HTTP. Jekyll, being
  flat files, is at least as secure as whatever you're syncing your site with,
  which in 2018 should be something more secure than FTP.

## Disadvantages of Jekyll

* __No default theme__: Jekyll provides no default theme. A Jekyll user is
  probably a programmer, not a website designer, meaning that good-looking
  Jekyll sites, while entirely possible, are rare. Wordpress, conversely, has a
  default theme and a wide selection of free and paid themes to choose from.
* __Requires technical skill__: Jekyll requires users to install and run a Ruby
  script (unless you use Github Pages, but then you have to learn git), upload
  to a webserver using something like git or rsync, and adhere to a strict
  filename convention and document format.. This is all explained in the
  documentation but not necessarily intuitive to new users.
* __Poor for multi-user__: The default Jekyll workflow is to edit the page, run
  Jekyll locally, then upload the resulting HTML. It's tricky for multiple users
  to keep this in sync, or for users to be given different access levels.
* __Poor category support__: Jekyll handles categories poorly. There is no such
  thing as a category page unless you manually create one, and no
  differentiation between category name and category slug (e.g. "Star Trek" and
  "startrek"), making it difficult to use in URLs. There is no robust mechanism
  for subcategories.
* __No date-based pages__: The default URL scheme is something like
  `2018/03/21/article-title.html`, but there is no page at, say, `2018/03/` or
  `2018/index.html`, which users have come to expect thanks to systems like
  Wordpress. You can create those pages, but it must be done manually.
* __No dynamic features__: Since it's all flat files, the server is unable to
  run more advanced features like comments, scheduled posts, search, or
  analytics. Some of these features can be recreated with Javascript or outside
  tools.
* __No RSS feed__: RSS functionality is not included by default, but can be
  added [pretty easily](https://github.com/orbitalflower/jekyll-rss).
* __Bad for remote editing__: Normally, you must edit and build the site
  locally, then upload that, whereas Github Pages will auto-compile your Jekyll
  site for you. Either way, however, you need Jekyll or git installed on the
  device you're editing from, along with a synced copy of your site source.
  That's less convenient than a web CMS which lets you log in.

## Summary

Jekyll is a secure, customizable and inexpensive way to publish webpages from
plain text with minimal markup, but it is not as powerful or convenient as a
true CMS, and lacks many features users have come to expect from something like
Wordpress.
