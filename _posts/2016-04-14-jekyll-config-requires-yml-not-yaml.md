---
title: "Jekyll config requires .yml, not .yaml"
category: comp
tags: jekyll
redirect_from:
- 20160414-jekyll-config-requires-yml-not-yaml.html
description: 
license: CC BY
---

I encountered a peculiar issue with GitHub's Pages' Jekyll handling recently.

The config file must be `_config.yml`, not `_config.yaml`.

Until recently, GitHub accepted both, even though the documentation gives the
`.yml` extension. This means if you were using .yaml for some reason, your blog
would break and revert to default settings.

Without a valid settings file, GitHub Pages will still build Jekyll pages
without an error, but the blog would lose its custom configuration.
