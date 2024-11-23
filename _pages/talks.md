---
layout: archive
title: "Presentations"
permalink: /talks/
author_profile: true
---

<style>
body {margin:25px;}
p {font-size: 12px;}

div.polaroid {
  width: 75%;
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
  <p>Lyzzett, Luis, Danna, and Fermin, participants in the <a href="https://sites.google.com/view/nsf-ires-softmatter">NSF IRES</a> program, presenting at the 2024 Frontiers in Soft Matter Conference.</p>
  </div>
</div>

<div class="polaroid">
  <img src="/images/gil - aps mm 2024 - mlddm talk.jpg" alt="Gil presenting at APS MM 2024" style="width:100%">
  <div class="container">
  <p><a href="/team/2023-06-01-GM" rel="permalink">Gil</a> presenting at the 2024 APS March Meeting.</p>
  </div>
</div>

<div class="polaroid">
  <img src="/images/laura and kayla - Fall 2024 OUR conf.jpg" alt="Fall 2024 OUR poster session" style="width:100%">
  <div class="container">
  <p><a href="/team/2023-08-01-LM" rel="permalink">Laura</a> and <a href="/team/2024-06-01-MB" rel="permalink">Kayla</a> presenting posters, September 2024.</p>
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