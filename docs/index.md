---
layout: default
title: Index
---
# Index page

{% for repository in site.github.public_repositories %}
  * [{{ repository.name }}]({{ repository.html_url }})
{% endfor %}

{% for category in site.categories %}
    <h2>{{ category[0] }}</h2>
    <ul>
        {% for post in category[1] %}
        <li>{{post.title}}</li>
        {% endfor %}
    </ul>
{% endfor %}


<ul>
    {% for category in site.data.categories %}
    <li>
        <a href="/Arduino/doc{{ category.file | slugify }}">
            {{ category.name }}
        </a>
    </li>
    {% endfor %}
</ul>




# Header 1
## Header 2
