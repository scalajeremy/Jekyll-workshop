# 6. Action

Let's play around a litte bit.

## Build your website

If it's not yet build

```bash
    jekyll serve
```

## Add some posts

Take a look to the **_posts** folder. There is a file that should look like that "*2019-06-24-welcome-to-jekyll.markdown*". This is a post, a news, an entry to your blog.
By default, Jekyll will show them to your homepage by date order.
For now, we'll just learn to make a new entry.

Open your favorite text/code editor and create a new file "**2019-06-25-workshop.md**"

Jekyll use something call **YAML Frontmatter**. It's some lines you have to put at the start of your file to let it know how it must show the page.

```yml
---
layout: post
title:  "I love this workshop"
date:   2019-06-25 09:00:00 +0200
categories: jekyll update
---
```

What it does?

**layout**: tell Jekyll which layout it should use to display this page. More on that later
**title**: really?
**date**: come on, it's just a date! :exclamation: Carefull with the format, I need to be: yyyy-mm-dd hh:mm:ss. You can't "program" a article to appear in a future date. If you put a date in the future, you'll still need to rebuild your site for your article to appear.
**categories**: here you can put some categories to organize your entries. It's optionnal.

Now that we tell Jekyll how to display this page, let's add some content. Everything should be done in markdown.

## Add some posts with Jekyll-admin

Now that you saw how Jekyll work, let's use Jekyll-admin to do exactly the same but without your favortie editor. :cry:
