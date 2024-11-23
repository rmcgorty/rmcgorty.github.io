---
layout: archive
title: "Presentations"
permalink: /talks/
author_profile: true
---

<style>
body {margin:25px;}
p {font-size: 10px;}

div.polaroid {
  width: 45%;
  background-color: white;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  margin-bottom: 25px;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

div.container {
  text-align: center;
  padding: 10px 20px;
}
</style>

<div class="polaroid">
  <img src="/images/Soft Matter 2024 - Lyzzett Luis Danna Fermin.jpg" alt="Frontiers in Soft Matter 2024" style="width:100%">
  <div class="container">
  <p>Students who participated in <a href="https://sites.google.com/view/nsf-ires-softmatter">NSF IRES</a> project presenting at the 2024 Frontiers in Soft Matter Conference.</p>
  </div>
</div>

<div class="polaroid">
  <img src="/images/gil - aps mm 2024 - mlddm talk.jpg" alt="Gil presenting at APS MM 2024" style="width:100%">
  <div class="container">
  <p><a href="/team/2023-06-01-GM" rel="permalink">Gil</a> project presenting at the 2024 APS March Meeting.</p>
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