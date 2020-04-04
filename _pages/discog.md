---
layout: default
title: Discog
permalink: /discog/
---

### Engineering/Mixing 

<br>

{% for credit in site.data.credits %}
  {% if credit.type == "record" %}

  <span class="credit-title">{{ credit.title }}</span> 
  <span class="credit-artist">{{ credit.artist }}</span>
  <span class="credit-year">{{ credit.year }}</span>{% if credit.released == "false" %}<span> release</span>{% endif %} {% if credit.mp3one != "false" %}<span class="credit-mp3"><a  href="{{ site.url | prepend: site.baseurl }}/assets/mp3/{{ credit.mp3one }}" target="_blank" type="audio/mp3">listen</a></span>{% endif %}
  {% if credit.mp3two != "false" %}<span class="credit-mp3"><a  href="{{ site.url | prepend: site.baseurl }}/assets/mp3/{{ credit.mp3two }}" target="_blank" type="audio/mp3">listen</a></span>{% endif %}
  {% endif %}
{% endfor %}

<br><br> 

### Film

<br> 

{% for credit in site.data.credits %}
  {% if credit.type == "short film" or credit.type == "documentary" %}
  <span class="credit-title">{{ credit.title }}</span>
  <span class="credit-type">{{ credit.type | capitalize }}</span> by <span class="credit-artist">{{ credit.artist }}</span>
  <span class="credit-year">{{ credit.year }}</span><br>
  {% endif %}
{% endfor %}

