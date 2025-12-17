---
layout: category
title: Conexiones
permalink: /categoria/conexiones/
category: Conexiones
---

<!-- Hero de categoría -->
<section class="hero">
  <h1>Conexiones</h1>
  <p class="lead">Amplia variedad de conexiones plásticas para sistemas hidráulicos, sanitarios e industriales. Diferentes tipos, diámetros y materiales.</p>
</section>

<!-- Lista de productos en esta categoría -->
<section class="grid">
  {% assign productos = site.products | where: "category", "Conexiones" | sort: "order" %}
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
