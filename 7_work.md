# Exercices

Here is some exercices to learn a bit more about how Jekyll works. For each of them, I'm gonna explain the purpose of it, then you can start searching [the doc](https://jekyllrb.com/docs/) or google it. I'll add some hints and a link to the answer. When you complete an exercice, take a look at the answser, some time there is more informations.

## List

1. [Get the theme files](#Get-the-theme-files)
2. [Add a link to your facebook page](#Add-a-link-to-your-facebook-page)
3. [Add the categories](#Add-the-categories)
4. Add a list of author
5. Change the layout

## Get the theme files

> Difficulty: :red_circle::black_circle::black_circle::black_circle::black_circle:

For these exercices we'll need to changes some lines in the default layout of the minima theme. So the easiest way to do that is to add these files into your folder project rather then have them in your gem folder.

> :bulb: Hint #1: You need a code to **returns** the location of the gem-based theme files.
>
> :bulb: Hint #2: You'll find it in the documentation, in the "theme" chapter.

> :heavy_exclamation_mark: Don't cut the files and folder you'll find, or other website you've created with Jekyll could not work properly anymore.

> :heavy_check_mark: [The answer](/answers/1_theme.md)

## Add a link to your facebook page

> Difficulty: :red_circle::red_circle::black_circle::black_circle::black_circle:

Let's start with something easy. Base on what we already seen, you should be able to add a link to your facebook.

> :bulb: Hint #1: There's already a link to Twitter & Github
>
> :bulb: Hint #2: It's in the `_config.yml` file

> :heavy_check_mark: [The answer](/answers/2_facebook.md). There is more infos.

## Add the categories

> Difficulty: :red_circle::red_circle::red_circle::black_circle::black_circle:

We've seen that you can add some categories to your posts, but if you look closely, they're not showing in the front page or in the post itself. And there is no page to show all of them.

Let's fix that.

* Check the doc [here](https://jekyllrb.com/docs/posts/)
* Create a new page for displaying all the categories
* Display the categories of a post in the homepage
* Display the categories of a post in the post page itself

> :bulb: Hint #1: You'll need this `site.categories`
>
> :bulb: Hint #2: Take a look at [this tutorial](https://blog.webjeda.com/jekyll-categories/)
>

> :heavy_check_mark: [The answer](/answers/3_categories.md).
