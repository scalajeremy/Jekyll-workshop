# How to create the page for all categories

If you took a look at [this tutorial](https://blog.webjeda.com/jekyll-categories/) it told you how to do it. Let's take a closer look.

```html
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

# How to show the category on the homepage 

