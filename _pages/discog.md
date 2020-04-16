---
layout: default
title: Discog
permalink: /discog/
---

### Engineering/Mixing 

<br>

{% for credit in site.data.credits %}
  {% if credit.type == "record" %}
<div class="row">
  <div class="col-5"> 
   <span class="credit-title">{{ credit.title }}</span> 
  </div>
  <div class="col-4"> 
   <span class="credit-artist">{{ credit.artist }}</span>
  </div>
  <div class="col-3"> 
   <span class="credit-year">{{ credit.year }}</span>{% if credit.released == "false" %}<span> release</span>{% endif %}
  </div>
</div>
{% endif %}
{% endfor %}

<br><br> 

<div class="row">
  <div class="col">
   <h3>Film</h3>
  </div>
</div>

<br> 

<div class="row">
{% for credit in site.data.credits %}
  {% if credit.type == "short film" or credit.type == "documentary" %}
  <div class="col-5"> 
   <span class="credit-title">{{ credit.title }}</span>
  </div>
  <div class="col-4"> 
   <span class="credit-type">{{ credit.type | capitalize }}</span> by <span class="credit-artist">{{ credit.artist }}</span>
  </div>
  <div class="col-3"> 
   <span class="credit-year">{{ credit.year }}</span>
  </div>
  {% endif %}
{% endfor %}
</div>
