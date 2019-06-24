# 4. Plugins

To use plugins, you need to add them to a Bundler group in your `Gemfile`. One usefull plugin is jekyll-admin so we will use it as an example.

```ruby
# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.6"
end
```

Here is your default plugin bundler with already a plugin inside.

What you need to do is just add the gem jekyll-admin inside the group.

```ruby
# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.6"
  gem "jekyll-admin"
end
```

And now you need to install it via terminal.

```bash
bundle install
```

Restart your Jekyll. That's all.

[More on installation of plugins](https://jekyllrb.com/docs/plugins/installation/)

For later, here is a list of some [usefull plugins](https://github.com/planetjekyll/awesome-jekyll-plugins)

## What is jekyll-admin and how to use it

A Jekyll plugin that provides users with a traditional CMS-style graphical interface to author content and administer of Jekyll sites.

Navigate to [http://localhost:4000/admin](http://localhost:4000/admin) to access the admin panel.

Note that this is stricly a local admin. No need to login!

## Next step : [5. config.yml & install a theme](5_theme.md)
