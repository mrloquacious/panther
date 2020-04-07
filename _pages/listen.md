---
layout: default
title: Listen
permalink: /listen/
---

{% for mp3 in site.data.listen %}
  <span class="credit-artist">{{ mp3.artist }}</span>
  <span class="credit-title">{{ mp3.title }}</span>{% if mp3.note != "false" %}<span> \*{{ mp3.note }}</span>{% endif %}
{% if mp3.mp3 != "false" %}<span class="credit-mp3"><a  href="{{ site.url | prepend: site.baseurl }}/assets/mp3/{{ mp3.mp3 }}" target="_blank" type="audio/mp3">listen</a></span>{% endif %}
{% endfor %}


