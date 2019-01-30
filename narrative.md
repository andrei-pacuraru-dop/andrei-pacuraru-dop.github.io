---
layout: gallery
title: Narrative Film
permalink: /narrative-film/
---

{% for video in site.narrative %}
    {% if video.youtube_id %}
<a href="https://www.youtube.com/watch?v={{ video.youtube_id }}">
   <img src="{{ video.image }}">
</a>
    {% elsif video.vimeo_id %}
<a href="https://vimeo.com/{{ video.vimeo_id }}">
   <img src="{{ video.image }}">
</a>
    {% endif %}
{% endfor %}
