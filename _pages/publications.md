---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% for post in site.publications reversed %}
{% assign currentdate = post.date | date: "%Y" %} {% if currentdate != date %} {% unless forloop.first %}

{% endunless %} <h2 id="y{{post.date | date: "%Y"}}">{{ currentdate }}
{% assign date = currentdate %} {% endif %} {% if post.authors contains 'McGorty' %} {% include archive-single-pub.html %} {% endif %} {% if forloop.last %}
{% endif %}
{% endfor %}
