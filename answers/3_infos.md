# To add some default values

Just add these lines in your `_config.yml`

```yml
defaults:
  -
    scope:
      path: "" # an empty string here means all files in the project
      type: "posts"
    values:
      layout: "post"
```

This is actually a really powerful feature. You can do much more but for now it'll be all.
