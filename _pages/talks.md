---
layout: archive
title: "Presentations"
permalink: /talks/
author_profile: true
---

<div class="polaroid">
  <img src="/images/Soft Matter 2024 - Lyzzett Luis Danna Fermin.jpg" alt="Frontiers in Soft Matter 2024" style="width:30%">
  <div class="container">
  <p>Students who participated in <a href="https://sites.google.com/view/nsf-ires-softmatter">NSF IRES</a> project presenting at the 2024 Frontiers in Soft Matter Conference.</p>
  </div>
</div>

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