---
layout: default
title: Photos
permalink: /photos/
---

<div id="myCarousel" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
  {% for pic in site.data.photo %}
   <div class="carousel-item {% if forloop.first %}active{% endif %}">
   <img src="/assets/photo/{{ pic.photo }}" class="d-block w-100 img-fluid" alt="Image of Panther PDX studio">
  </div>
  {% endfor %}
  </div>
  <a class="carousel-control-prev" href="#myCarousel" role="button" data-slide="prev" onclick="$('#myCarousel').carousel('prev')">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#myCarousel" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

<a class="left carousel-control" href="#myCarousel" data-slide="prev" onclick="$('#myCarousel').carousel('prev')">‹</a>

