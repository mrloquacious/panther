---
layout: default
title: Gear
permalink: /gear/
---

{% comment %}
{% assign monitoring = site.data.gear | where: "type", "monitoring" %}
{% for item in site.data.gear %}
{% endfor %}
{% endcomment %}

{% for category in site.data.geartype %}
  <h3>{{ category.geartype | upcase }}</h3>
    {% for item in site.data.gear %}
      {% if item.type == category.geartype %}
   <span class="gear-name">{{ item.name }}</span>{% if item.checkavail == "true" %}<span>\*</span>{% endif %} <br>
      {% endif %}
    {% endfor %}
   <br>
{% endfor%}

\* Check Availability

<br><br>

{% comment %}
## Monitoring
## A/D Converters
## DAW
## Outboard/Hardware
## Microphones
## Plug Ins
## Guitars
## Amps
## Keys
## Drums/Percussion
## Other
{% endcomment %}
