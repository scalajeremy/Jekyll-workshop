# 5. Install a theme and a quicklook into the config.yml

## Install a gem-based theme
To install a gem-based theme you need to :
* Add it to your Gemfile and remove the ancient default theme

```Ruby
# This is the default theme for new Jekyll sites. You may change this to anything you like.
    - gem "minima", "~> 2.0"
    + gem "jekyll-theme-minimal"
```
* Install it

```bash
    bundle install
```
* Add it to the _config.yml to activate it
```yml
# Build settings
    markdown: kramdown
    theme: jekyll-theme-minimal
```

* Build your site
```bash
    bundle exec jekyll serve
```
:exclamation: You can have multiple themes listed in your site’s Gemfile, but only one theme can be selected in your site’s _config.yml.



## A quick look into the _config.yml

The _config.yml is meant for settings that affect your whole blog, values which you are expected to set up once and rarely edit after that. So let's start and simply read the comments who are pretty explicites.

```yml 
# Site settings
# These are used to personalize your new site. If you look in the HTML files,
# you will see them accessed via {{ site.title }}, {{ site.email }}, and so on.
# You can create any custom variable you would like, and they will be accessible
# in the templates via {{ site.myvariable }}.
title: Your awesome title
email: your-email@example.com
description: >- # this means to ignore newlines until "baseurl:"
  Write an awesome description for your new site here. You can edit this
  line in _config.yml. It will appear in your document head meta (for
  Google search results) and in your feed.xml site description.
baseurl: "" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site, e.g. http://example.com
twitter_username: jekyllrb
github_username:  jekyll

# Build settings
markdown: kramdown
theme: minima
plugins:
  - jekyll-feed

# Exclude from processing.
# The following items will not be processed, by default. Create a custom list
# to override the default setting.
# exclude:
#   - Gemfile
#   - Gemfile.lock
#   - node_modules
#   - vendor/bundle/
#   - vendor/cache/
#   - vendor/gems/
#   - vendor/ruby/
```