---
layout: gallery
title: Narrative Film
permalink: /narrative
embed_video_mp4: http://shepherdtone.co.uk/media/video.mp4
embed_video_ogg: http://shepherdtone.co.uk/media/video.ogv
placeholder: http://shepherdtone.co.uk/media/still1.jpg
---

<div class="video-gallery">
{% for video in site.narrative %}
  {% assign mod = forloop.index0 | modulo : 3 %}
  {% if mod == 0 %}
<div class="inner">
  {% endif %}
<a href="{{ video.url }}">
  <img src="{{ video.thumb }}">
</a>
  {% if mod == 2 %}
</div>
  {% endif %}
{% endfor %}
</div>


