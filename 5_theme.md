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