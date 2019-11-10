---
layout: gallery
title: Narrative Film
permalink: /narrative
vimeo_id: 332521900
placeholder: /assets/img/full/Ishtar_FS.png
---

<div class="video-gallery">
{% for video in site.narrative %}
  {% assign mod = forloop.index0 | modulo : 3 %}
  {% if mod == 0 %}
<div class="inner">
  {% endif %}
<a href="{{ video.url }}">
  <img src="{{ video.thumb }}">
  <h2 class="text-center">{{ video.title }}</h2>
  <h4 class="text-center">Dir. {{ video.dir }}</h4>
</a>
  {% if mod == 2 %}
</div>
  {% endif %}
{% endfor %}
</div>


