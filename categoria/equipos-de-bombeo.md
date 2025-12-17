---
layout: category
title: Equipos de bombeo
permalink: /categoria/equipos-de-bombeo/
category: Equipos de bombeo
---

<!-- Hero de categoría -->
<section class="hero">
  <h1>Equipos de bombeo</h1>
  <p class="lead">Soluciones de bombeo para agua, químicos y procesos industriales. Bombas centrífugas, sumergibles y sistemas de presión.</p>
</section>

<!-- Lista de productos en esta categoría -->
<section class="grid">
  {% assign productos = site.products | where: "category", "Equipos de bombeo" | sort: "order" %}
  {% for p in productos %}
    <article class="card">
      <a class="card-media" href="{{ p.url | relative_url }}">
        {% if p.image %}
          <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
        {% endif %}
      </a>
      <div class="card-body">
        <h3 class="card-title"><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
        {% if p.summary %}
          <p class="card-text">{{ p.summary }}</p>
        {% endif %}
        <a class="button" href="{{ p.url | relative_url }}">Ver detalles</a>
      </div>
    </article>
  {% endfor %}
</section>
