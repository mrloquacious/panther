---
layout: default
title: Listen
permalink: /listen/
---

<div class="row mt-2">
  <div class="col">
   <h3>Recorded and Mixed by Steve Drizos</h3> 
   <p>(Click song title to listen)</p>
  </div>
</div>  

{% for mp3 in site.data.listen %}
  {% if mp3.recorded == "true" %}
<div class="row mt-2">
  <div class="col">
   <span class="listen-artist">{{ mp3.artist }}</span>
  </div>
  <div class="col">
   <a href="{{ site.url | prepend: site.baseurl }}/assets/mp3/{{ mp3.mp3 }}" target="_blank" type="audio/mp3">
      <span class="listen-title">{{ mp3.title }}</span>{% if mp3.note != "false" %}&nbsp;<span>*</span>{% endif %}
   </a>
  </div>
</div>
  {% endif %}
{% endfor %}

<br>

<div class="row mt-2">
  <div class="col">
   <h3>Mixed by Steve Drizos</h3>
  </div>
</div>  

{% for mp3 in site.data.listen %}
  {% if mp3.recorded == "false" %}
<div class="row mt-2">
  <div class="col">
   <span class="listen-artist">{{ mp3.artist }}</span>
  </div>
  <div class="col">
   <a  href="{{ site.url | prepend: site.baseurl }}/assets/mp3/{{ mp3.mp3 }}" target="_blank" type="audio/mp3">
     <span class="listen-title">{{ mp3.title }}</span>   
   </a>
  </div>
</div>
  {% endif %}
{% endfor %}

<br><br>

{% for mp3 in site.data.listen %}
  {% if mp3.note != "false" %}<span> \*{{ mp3.note }}</span>{% endif %}
{% endfor %}


