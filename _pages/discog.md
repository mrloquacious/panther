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
  <span class="credit-year">{{ credit.year }}</span>{% if credit.released == "false" %}<span> release</span>{% endif %}
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

