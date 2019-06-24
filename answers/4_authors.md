# How to create the list for all authors

Here is an example of code to do it.

Make an authors.yml file in `_data` folder

```yml
- name: Eric Mill
  

- name: Parker Moore
  

- name: Liu Fengyun
  
```

Now you can use it in your template.

```html
<ul>
 {% for author in site.data.authors %}
    <li>
        {{ author.name }}
    </li>
    {% endfor %}
</ul>
```

 # How to show the authors on the homepage and post page

Open `post.html` in `_layouts` folder then add these lines

```html
<div class="post-authors">
  {% if post %}
    {% assign authors = post.authors %}
  {% else %}
    {% assign authors = page.authors %}
  {% endif %}
  {% for author in authors %}
  <a href="{{site.baseurl}}/authors/#{{author|slugize}}">{{author}}</a>
  {% unless forloop.last %}&nbsp;{% endunless %}
  {% endfor %}
</div>
```

## [Return to the exercices](../7_work.md#4-Add-a-list-of-authors)
