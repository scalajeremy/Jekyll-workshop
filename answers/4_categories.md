# How to create the page for all categories

If you took a look at [this tutorial](https://blog.webjeda.com/jekyll-categories/) it told you how to do it. Let's take a closer look.

#### category.html

```html
---
layout: page
permalink: /categories/
title: Categories
---
<div id="archives">
{% for category in site.categories %} <!-- Do something for each category -->
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %} <!-- Get the first category -->
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h3 class="category-head">{{ category_name }}</h3> <!-- Show the category name -->
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %} <!-- Do something for every post there is in this category -->
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4> <!-- Show a post -->
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>
```

It's just a for loop, done with [Liquid](https://jekyllrb.com/docs/liquid/). If you want to know more about it, you'll need to learn it by yourself, sorry.

# How to show the category on the homepage and post page.

Open `post.html` in `_layouts` folder then add these lines

```html
<div class="post-categories">
  {% if post %}
    {% assign categories = post.categories %}
  {% else %}
    {% assign categories = page.categories %}
  {% endif %}
  {% for category in categories %}
  <a href="{{site.baseurl}}/categories/#{{category|slugize}}">{{category}}</a>
  {% unless forloop.last %}&nbsp;{% endunless %}
  {% endfor %}
</div>
```

## [Return to the exercices](../7_work.md#3-Add-the-categories)
