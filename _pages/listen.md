---
layout: default
title: Listen
permalink: /listen/
---

### Recorded and Mixed by Steve Drizos  

{% for mp3 in site.data.listen %}
  {% if mp3.recorded == "true" %}
<div class="row">
  <div class="col-4">
   <a href="{{ site.url | prepend: site.baseurl }}/assets/mp3/{{ mp3.mp3 }}" target="_blank" type="audio/mp3">
     <span class="credit-title">{{ mp3.title }}</span>{% if mp3.note != "false" %} <span>*</span>{% endif %}
   </a>
  </div>
  <div class="col-8"><span class="credit-artist">{{ mp3.artist }}</span>
  </div>
</div>
  {% endif %}
{% endfor %}

<br>

### Mixed by Steve Drizos  

{% for mp3 in site.data.listen %}
  {% if mp3.recorded == "false" %}
<div class="row">
  <div class="col-4">
   <a  href="{{ site.url | prepend: site.baseurl }}/assets/mp3/{{ mp3.mp3 }}" target="_blank" type="audio/mp3">
     <span class="credit-title">{{ mp3.title }}</span>
   </a>
  </div>
  <div class="col-8">
   <span class="credit-artist">{{ mp3.artist }}</span>
  </div>
</div>
  {% endif %}
{% endfor %}

<br><br>

{% for mp3 in site.data.listen %}
  {% if mp3.note != "false" %}<span> \*{{ mp3.note }}</span>{% endif %}
{% endfor %}


