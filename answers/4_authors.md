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
