# Exercices

Here is some exercices to learn a bit more about how Jekyll works. For each of them, I'm gonna explain the purpose of it, then you can start searching [the doc](https://jekyllrb.com/docs/) or google it. I'll add some hints and a link to the answer. When you complete an exercice, take a look at the answser, some time there is more informations.

## List of exercices

- [1. Get the theme files](#1-Get-the-theme-files)
- [2. Add a link to your facebook page](#2-Add-a-link-to-your-facebook-page)
- [3. Change basics infos of your site](Change-basics-infos-of-your-site-and-make-some-defaults-settings)
- [4. Add the categories](#4-Add-the-categories)
- [5. Add a list of authors](#5-Add-a-list-of-authors)
- [6. Be crazy](#6-Be-crazy)
- [Bonus: FTP & Github page](#Bonus)

## 1. Get the theme files

> Difficulty: :red_circle::black_circle::black_circle::black_circle::black_circle:

For these exercices we'll need to changes some lines in the default layout of the minima theme. So the easiest way to do that is to add these files into your folder project rather then have them in your gem folder.

> :bulb: Hint #1: You need a code to **returns** the location of the gem-based theme files.
>
> :bulb: Hint #2: You'll find it in the documentation, in the "theme" chapter.

> :heavy_exclamation_mark: Don't cut the files and folder you'll find, or other website you've created with Jekyll could not work properly anymore.

> :heavy_check_mark: [The answer](/answers/1_theme.md)

## 2. Add a link to your facebook page

> Difficulty: :red_circle::black_circle::black_circle::black_circle::black_circle:

Let's start with something easy. Base on what we already seen, you should be able to add a link to your facebook.

> :bulb: Hint #1: There's already a link to Twitter & Github
>
> :bulb: Hint #2: It's in the `_config.yml` file

> :heavy_check_mark: [The answer](/answers/2_facebook.md). There is more infos.

## 3. Change basics infos of your site and make some defaults settings

> Difficulty: :red_circle::red_circle::black_circle::black_circle::black_circle:

You just edit the `_config.yml` file, maybe you noticed some other stuff in there... Let's change your title, description and email. Look for your changes.

Now we'll do something usefull for Jekyll-Admin, we'll set some default value, so you can't forget to put the layout.

> :bulb: Hint #1: you're gonna need this [in the doc](https://jekyllrb.com/docs/configuration/front-matter-defaults/)

> :heavy_check_mark: [The answer](/answers/3_infos.md).

## 4. Add the categories

> Difficulty: :red_circle::red_circle::red_circle::black_circle::black_circle:

We've seen that you can add some categories to your posts, but if you look closely, they're not showing in the front page or in the post itself. And there is no page to show all of them.

Let's fix that.

* Check the doc [here](https://jekyllrb.com/docs/posts/)
* Create a new page for displaying all the categories
* Display the categories of a post in the homepage
* Display the categories of a post in the post page itself

> :bulb: Hint #1: You'll need to create a new html page at the root folder.
>
> :bulb: Hint #2: You'll need this `site.categories`, `post.categories`, `page.categories`,...
>
> :bulb: Hint #3: You'll need to use [Liquid](https://jekyllrb.com/docs/liquid/) templating engine.
>
> :bulb: Hint #4: Take a look at [this tutorial](https://blog.webjeda.com/jekyll-categories/)
>

> :heavy_check_mark: [The answer](/answers/4_categories.md).

## 5. Add a list of authors

> Difficulty: :red_circle::red_circle::red_circle::black_circle::black_circle:

Ok so now that we have some articles in categories, we may want to show the authors of each and a list of authors. 

Let's do it.

* Create a new page for displaying all the authors
* Display the author of a post in the homepage
* Display the author of a post in the post page itself


> :bulb: Hint #1: It's almost the same as for the categories. But you'll need to use Data File to stock all the members
>
> :bulb: Hint #2: Check the doc [here](https://jekyllrb.com/docs/datafiles/) but not too quickly at the example

> :heavy_check_mark: [The answer](/answers/5_authors.md).


## 6. Be crazy

> Difficulty: :red_circle::red_circle::red_circle::red_circle::black_circle:

Now that you've seen how Jekyll work and how you can customize it, let's get creative and change the template.

[Install a theme](5_theme.md#Install-a-gem-based-theme)

[Install another plugin](4_plugins.md)

Here is some information about files of a theme:

Files                                       | What he does
------------                                | -------------
/_includes/diqsus_comments.html             | Display comments from [Disqus](https://disqus.com/) if enable
/_includes/footer.html                      | Display the footer
/_includes/google-analytics.html            | Enable Google Analytics
/_includes/head.html                        | Add <head> tag for all pages
/_includes/header.html                      | Display the header of your theme
/_includes/icon-github.html                 | Tell how the icon of Github should be working (link,...)
/_includes/icon-github.svg                  | SVG for the logo of Github
/_includes/icon-twitter.html                | Tell how the icon of Twitter should be working (link,...)
/_includes/icon-twitter.svg                 | SVG for the logo of Twitter
/_includes/socials.html                     | Display the icons of all socials web site who has been enable
------------                                | ------------   
/_layouts/default.html                      | A default template of your pages (html, body, "includes",...)
/_layouts/home.html                         | A default template for the homepage.
/_layouts/page.html                         | A default template for displaying every page.
/_layouts/post.html                         | A default template for displaying every posts.
------------                                | ------------   
/_sass/minima.scss                          | The compiled sass file for styling the theme.
/_sass/minima/_bases.scss                   | Sass file with the basics styling (like body, font, h,...)
/_sass/minima/_layout.scss                  | Sass file with everything usefull for the layouts
/_sass/minima/_syntax-highlighting.scss     | Sass file with some syntax higlight for codes

But there can be more of them. It depends on the theme you get. But in brief:

* In `_layouts` you can add all the html you need for creating differents page layout. Imagine you want a post to appear different for a certain category, you can just create a new layout called `post-different.html` and now in your Frontmatter you just need to add `layout: post-different`
* In `_includes` you can add html pages for everything you need to call on your theme and that can be repeated. For example: you want to add a navbar, you can add it to `header.html` or create a seperate file `navbar.html`. If you do a new file, you must add something like this to `default.html`

```liquid
{%- include navbar.html -%}
```

* In `_sass` you put your `.scss` files for the theme. Jekyll will compile it everytime you run `bundle exec jekyll serve`.

## Bonus

Github page

FTP
