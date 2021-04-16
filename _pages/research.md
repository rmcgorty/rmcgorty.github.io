---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---
{% include base_path %}

<div class="grid">
  <div class="wrapper">
    {% for post in site.research %}
      {% include archive-single-proj.html type="grid" %}
    {% endfor %}
  </div>
</div>
