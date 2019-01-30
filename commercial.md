---
layout: gallery
title: Commercial
permalink: /commercial/
---


<div class="wrapper">
<h1 class="text-center">{{ page.title }}</h1>
<p>&nbsp;</p>
</div>

<div class="video-gallery">
{% for video in site.commercial %}
	{% assign mod = forloop.index0 | modulo : 3 %}
    {% if mod == 0 %}
<div class="inner">
	{% endif %}
    {% if video.youtube_id %}
<a href="https://www.youtube.com/watch?v={{ video.youtube_id }}">
   <img src="{{ video.image }}">
</a>
    {% elsif video.vimeo_id %}
<a href="https://vimeo.com/{{ video.vimeo_id }}">
   <img src="{{ video.image }}">
</a>
    {% endif %}
    {% if mod == 2 %}
</div>
	{% endif %}
{% endfor %}
</div>
