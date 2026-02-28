---
title: "Making a website with Jekyll and GitHub Pages"
category: comp
tags: web
redirect_from:
- /comp/web/website-jekyll-github-pages.html
description: "A guide to running a website like this one."
---

In the early days of the web, running your own website meant writing pages in
HTML and uploading them with FTP to a web server. The now-ubiquitous Wordpress
did not exist until 2003, and Twitter was not launched until 2006. Nowadays,
most people's web presence consists of accounts on social media, but there's
nothing stopping you from making a website the old-fashioned way.

If you're interested in making your own website, a modern, convenient, and free
of charge approach is to use [Jekyll](https://jekyllrb.com/)
and [GitHub Pages](https://pages.github.com/). Having run such a site for
several years, I've written this guide to anyone who'd like to start.

1. Table of Contents
{:toc}

## Overview

Jekyll is a Ruby program to convert Markdown text into HTML and apply
user-supplied page templates, plus some other conveniences. In short, you can
write in plain text with very simple formatting syntax and have it converted
into your website.

GitHub is a popular and free-of-charge site for hosting programming projects and
source code. It also runs GitHub Pages, a service for hosting the project
website, although you can also simply host a personal homepage there. GitHub
Pages will automatically convert a Jekyll setup into HTML, so you don't even
need to run Jekyll locally.

_Disclaimer:_ Although I've been using GitHub Pages with Jekyll for several
years, I'm not a git expert. If the advice given here for setting up git and
GitHub is insufficient, you can find numerous much better git tutorials online.

## Starting with Git and GitHub

You can skip this section if you are already familiar with using GitHub.

Git is a content versioning system used for syncing copies of source code
repositories. It provides a secure way of transferring a local copy of a website
to a web server such as GitHub, a popular site which hosts git repositories.

GitHub has advice on [setting up SSH authentication](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh).

1. Install git. On Windows, use the [git Windows download page](https://git-scm.com/download/win).
On Linux, it's available via your package manager (e.g. `apt install git`).
2. [Join GitHub](https://github.com/join).
3. [Generate an SSH key](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
4. [Add the SSH public key](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account) to your GitHub account.
5. Configure git locally to use your GitHub account's username email address;
e.g. `git config user.name username` and `git config user.email
username@users.noreply.github.com`, replacing "username" with your username.

## Setting up your repository

On the GitHub website, create a repository for your website. The instructions
appear on the [GitHub Pages](https://pages.github.com/) website. The name of the
repository should be your own GitHub username followed by `.github.io`, e.g.
`username.github.io`. The website will be at `https://username.github.io`.

You will see some online guides say that you have to install Ruby and Jekyll on
your local PC. This isn't necessary. GitHub pages can be set to run Jekyll
automatically on the server.

In the settings for your repository, select the Pages tab to configure GitHub
pages. I recommend selecting the `main` branch and `/ (root)` folder, since
this repository will only be used to contain the website.

Sync the online repository to a local copy, e.g.:

```
git clone https://github.com/username/username.github.io 
```

## Setting up Jekyll folder

You don't need to install Jekyll locally. You just need to set up a folder with
a [Jekyll directory structure](https://jekyllrb.com/docs/structure/).

The basic folder setup only requires a `_config.yml`, a `_posts` folder for your
articles, a `_layouts` folder for your page theme templates, and an `index.md` or
`index.html` for your main page. You might also want other files used by your
theme, like a `style.css`, `favicon.ico`, and images. It's also nice to have a
`readme.md`.

`_config.yml` (note the leading underline) is your config file. At minimum,
this should contain your title and site description, but you will also want to
set up the [permalink format](https://jekyllrb.com/docs/permalinks/) used by
posts.

```
title: Bob's Homepage
description: The personal website of Bob.
permalink: ordinal
plugins:
  - jekyll-feed
```

As for themes, you can grab an existing theme from a site like [Dr. Jekyll's
Themes](https://drjekyllthemes.github.io/) or any other [Jekyll theme
sites](https://jekyllrb.com/docs/themes/). You can of course read the docs and
make your own theme.

To sync this to GitHub:

```
git add *
git commit -am ""
git push origin main
```

## Writing pages

There are two types of content in Jekyll: [pages](https://jekyllrb.com/docs/pages/),
and [posts](https://jekyllrb.com/docs/posts/). The difference is
that posts have a date. Posts are useful for things like blog articles.

Posts require a particular filename format. Suppose you want a post dated July
19, 2021, titled "Useful NetHack strategies". The filename will be this:

```
2021-07-19-useful-nethack-strategies.md
```

The file must also start with a [front matter](https://jekyllrb.com/docs/front-matter/)
block in order to be parsed. For example:

```
---
layout: post
title: Useful NetHack strategies
---

Here is a list of strategies I have found useful in the game NetHack.

## Strategy 1: Chug from fountains like a crazy person...
```

The "layout" property determines which template in `_layouts` is used. As I'll
explain later, you can configure Jekyll to always use a certain one by default,
which is a good idea so that you don't have to type "layout: post" for every
post.

The URL which this appears at depends on the permalink format you set up in
`_config.yml`.

Files are written in Markdown.

Pages are similar, but don't require a date at the start, and don't have a date
associated with them. You can put them anywhere in the URL structure and they
will be recognized as long as they have front matter. Hence `index.md` in the
main directory will be transformed into an `index.html`.

## Syncing to GitHub

Your webpage is automatically re-parsed when synced to GitHub. It may take a few
moments for the page to update. You can skip the following advice if you're
already familiar with git and GitHub.

Adding a new file to GitHub requires three stages:

1. When a new file is first created, you have to _add_ it to the repository,
   otherwise it won't be synced
2. When one or more files are updated, you must _commit_ them to the repository,
   and the commit must have a description to say what was changed
3. To sync your repository to the GitHub server, you must _push_.

For example, we make an article:

```
git add _posts/2021-07-19-useful-nethack-strategies.md
git commit -m "new nethack article"
git push origin main
```

To save effort, you can add multiple files at once, and you can automatically
commit all previously added files with `-a`:

```
git add _posts/
git add *
git commit -am "changed something idk"
git push origin main
```

You can also check what changes have been made or have yet to be made:

```
git status
```

If this doesn't work, look up general git and GitHub tutorials for your
platform.

## Advanced and optional Jekyll features
### Don't upload drafts

You may want to exclude your unfinished drafts from being accidentally synced.
Just keep them in a `_drafts/` folder and add them to a .gitignore file:

```
_drafts/
Thumbs.db
*.pyc
```

### Default template

You probably don't want to have to add "layout: post" to the front of all your
posts. One way to do this is to set defaults in your `_config.yml`:

```
defaults:
  -
    scope:
      path: ""
    values:
      layout: "default"
```

However, an easier way is to use the 
[jekyll-default-layout](https://github.com/benbalter/jekyll-default-layout)
plugin by adding it to your `_config.yml`, e.g:

```
plugins:
  - jekyll-feed
  - jekyll-default-layout
```

This plugin will cause all posts to use "layout: post" by default, all pages to
use "layout: page" by default, and cause "index.md" to use "layout: home" or
"layout: page". If those templates don't exist, it falls back on "layout:
default". You can quite easily have your index page be an empty file except for
the title.

### Other convenient plugins

- `jekyll-optional-front-matter` lets you leave out the front matter section.
- `jekyll-titles-from-headings` automatically takes the first page heading as
  its title, and works well with `jekyll-optional-front-matter`.
- `jekyll-relative-links` automatically fixes links to other posts so that they
  show the correct URL.
- `jekyll-feed` generates an RSS feed. You will still need to add a link to your
  feed to your template.
- `jekyll-redirect-from` is really useful if you ever change your permalink
  format.
- `jemoji` handles emoji.
- `jekyll-seo-tag` and `jekyll-sitemap` are also supported, though I don't use
  them.

### Table of contents

You can manually add a table of contents to a page:

```
1. Table of Contents
{:toc}
```

### Using your own domain

See [Configuring a custom domain for your GitHub Pages
site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
You can even have HTTPS on your own domain.

## Advantages and disadvantages of using Jekyll

GitHub Pages with Jekyll is free of cost, supports HTTPS, can be edited offline,
and is secure. You can run a website without even using cookies, and configure
the layout however you wish. It's easy to export or back up your site because
it's just plain text.

The main drawbacks are that you have to learn basic git and have git installed
on the device you're editing from, things like category pages and such are kind
of awkward to implement, and you don't have certain server-side features like
comments.

See [The pros and cons of blogging with Jekyll](../comp/blogging-with-jekyll.html).
