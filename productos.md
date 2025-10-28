---
layout: default
title: "Productos"
permalink: /productos/
---

<h1>Catálogo por mercado</h1>
<p class="lead">Explora nuestras líneas y encuentra el producto adecuado según la aplicación.</p>

<!-- Botones de mercados -->
<div class="reveal" style="display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px;margin:16px 0 28px">
  <a class="button" href="{{ '/mercado/edificacion/' | relative_url }}">Edificación</a>
  <a class="button" href="{{ '/mercado/infraestructura/' | relative_url }}">Infraestructura</a>
  <a class="button" href="{{ '/mercado/industria/' | relative_url }}">Industria</a>
</div>

<h2 class="reveal">Todos los productos</h2>
<div class="grid reveal">
  {% assign productos = site.products | sort: 'order' %}
  {% for p in productos %}
  <article class="card">
    <a class="card-media" href="{{ p.url | relative_url }}">
      {% if p.image %}
      <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
      {% endif %}
    </a>
    <div class="card-body">
      <h3 class="card-title"><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
      {% if p.summary %}<p class="card-text">{{ p.summary }}</p>{% endif %}
      {% if p.market or p.category %}
      <p class="card-text" style="opacity:.8">
        {% if p.market %}{{ p.market }}{% endif %}{% if p.market and p.category %} · {% endif %}{% if p.category %}{{ p.category }}{% endif %}
      </p>
      {% endif %}
      <a class="button" href="{{ p.url | relative_url }}">Ver detalles</a>
    </div>
  </article>
  {% endfor %}
</div>
