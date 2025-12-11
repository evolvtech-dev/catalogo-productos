---
layout: default
title: "Productos"
permalink: /productos/
---

<section class="hero">
  <h1>Catálogo de Productos</h1>
  <p class="lead">Soluciones confiables en termoplásticos para edificación, industria e infraestructura.</p>
</section>

<div class="grid">
  {% assign productos = site.products | sort: 'order' %}
  {% for p in productos %}
  <article class="card">
    <a class="card-media" href="{{ p.url | relative_url }}">
      {% if p.image %}
      <img src="{{ p.image | relative_url }}" alt="{{ p.title }}" loading="lazy">
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
</div>
