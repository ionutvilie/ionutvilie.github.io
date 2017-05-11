---
layout: page
title: Feed
permalink: /
---
{% for post in site.posts limit: 3 %}
<a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
---
<p class="description">
    {% if post.description %}
        {{ post.description | strip_html | strip_newlines | truncate: 250 }}
    {% else %}
        {{ post.content | strip_html | strip_newlines | truncate: 500 }}
    {% endif %}</p>
{% endfor %}
---
