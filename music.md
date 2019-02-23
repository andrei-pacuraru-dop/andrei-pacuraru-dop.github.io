---
layout: gallery
title: Music Videos
permalink: /music-videos/
embed_video_mp4: http://shepherdtone.co.uk/media/video.mp4
embed_video_ogg: http://shepherdtone.co.uk/media/video.ogv
placeholder: http://shepherdtone.co.uk/media/still1.jpg
---

<div class="video-gallery">
{% for video in site.music %}
  {% assign mod = forloop.index0 | modulo : 3 %}
  {% if mod == 0 %}
<div class="inner">
  {% endif %}
<a href="{{ video.url }}">
  <img src="{{ video.image }}">
</a>
  {% if mod == 2 %}
</div>
  {% endif %}
{% endfor %}
</div>


