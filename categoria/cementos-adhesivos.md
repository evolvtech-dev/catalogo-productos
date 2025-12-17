---
layout: category
title: Cementos y adhesivos
permalink: /categoria/cementos-adhesivos/
category: Cementos y adhesivos
---

<!-- Hero de categoría -->
<section class="hero">
  <h1>Cementos y adhesivos</h1>
  <p class="lead">Cementos solventes, limpiadores y adhesivos industriales para asegurar uniones seguras y duraderas en sistemas plásticos.</p>
</section>

<!-- Lista de productos en esta categoría -->
<section class="grid">
  {% assign productos = site.products | where: "category", "Cementos y adhesivos" | sort: "order" %}
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
