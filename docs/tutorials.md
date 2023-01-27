---
layout: default
title: Tutorials
nav_order: 2
---
# Tutorials

{% assign postsByYear =
    site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
<ul>
{% for year in postsByYear %}
<li><a href="{{ site.url}}{{ page.url }}#{{ year.name }}">{{ year.name }}</a></li>
{% endfor %}
</ul>

---



<ul>
{% for year in postsByYear %}
  <h1 id = "{{ year.name }}">{{ year.name }}</h1>
    <ul>
      {% for post in year.items %}
        <li><a href="{{ post.url }}">{{ post.title }}-{{ post.date | date: "%B %-d, %Y"}}</a></li>
        {{ post.excerpt }}
        <p><a href="{{ post.url }}">(Read more...)</a></p>
      {% endfor %}
    </ul>
{% endfor %}

</ul>