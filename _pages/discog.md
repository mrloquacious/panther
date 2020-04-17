---
layout: default
title: Discog
permalink: /discog/
---

<div class="row mt-2">
  <div class="col">
   <h3>Engineering/Mixing</h3>
  </div>
</div>

{% for credit in site.data.credits %}
  {% if credit.type == "record" %}
<div class="row mt-2">
<div class="col-lg-4 col-md-5 col-sm-4 col-xs-12">
   <span class="credit-title">{{ credit.title }}</span> 
</div>
<div class="col-lg-4 col-md-4 col-sm-4 hidden-xs">
   <span class="credit-artist">{{ credit.artist }}</span>
</div>
<div class="col-lg-4 col-md-3 col-sm-4 hidden-xs">
   <span class="credit-year">{{ credit.year }}</span>{% if credit.released == "false" %}<span> release</span>{% endif %}
</div>
</div>
{% endif %}
{% endfor %}

<br><br> 

<div class="row mt-2">
  <div class="col">
   <h3>Film</h3>
  </div>
</div>

{% for credit in site.data.credits %}
  {% if credit.type == "short film" or credit.type == "documentary" %}
<div class="row mt-2">
  <div class="col-lg-4 col-md-5 col-sm-4 col-xs-12">
   <span class="credit-title">{{ credit.title }}</span>
  </div>
  <div class="col-lg-4 col-md-4 col-sm-4 hidden-xs">
   <span class="credit-type">{{ credit.type | capitalize }}</span> by <span class="credit-artist">{{ credit.artist }}</span>
  </div>
  <div class="col-lg-4 col-md-3 col-sm-4 hidden-xs">
   <span class="credit-year">{{ credit.year }}</span>
  </div>
</div>
  {% endif %}
{% endfor %}
