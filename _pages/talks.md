---
layout: archive
title: "Presentations"
permalink: /talks/
author_profile: true
---

<ul style="margin:0;padding:0">
{% for post in site.talks reversed %}

  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
    <h2 id="y{{post.date | date: "%Y"}}"><span style="color:gray">{{ currentdate }}</span></h2>
    <ul style="margin:0;padding:0">
    {% assign date = currentdate %}
  {% endif %}
  {% if post.authors contains 'McGorty' %}
    {% include archive-single-talk.html %}
  {% endif %}
  {% if forloop.last %}</ul>{% endif %}

{% endfor %}