---
layout: archive
permalink: /computer-science/
title: "Computer Science Work Terms"
author_profile: true
---
{% include group-by-array collection=site.posts field="tags" %}
{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
    {% if post.tag == "cs" %}
    <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
    {% endif %}
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}