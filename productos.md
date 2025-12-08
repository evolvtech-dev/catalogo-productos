---
layout: default
title: "Catálogo de Productos"
---

<section class="hero">
  <h1>Catálogo de Productos</h1>
  <p class="lead">Explora nuestras soluciones organizadas por industria y categoría.</p>
</section>

<!-- FILTROS POR INDUSTRIA -->
<nav class="filtros-industria" style="margin-bottom:24px; display:flex; flex-wrap:wrap; gap:12px">
  {% assign industrias = "Edificacion,Industria,Infraestructura,Agricola,Mineria,Quimica" | split: "," %}
  {% for industria in industrias %}
    <a class="button" href="#{{ industria | downcase }}">{{ industria }}</a>
  {% endfor %}
</nav>

<!-- AGRUPADOS POR INDUSTRIA -->
{% for industria in industrias %}
  <section id="{{ industria | downcase }}">
    <h2>{{ industria }}</h2>
    {% assign productos_industria = site.products | where: "market", industria %}
    
    {% assign categorias = productos_industria | map: "category" | uniq | sort %}
    
    {% for categoria in categorias %}
      <h3 style="margin-top:24px">{{ categoria }}</h3>
      <div class="grid">
        {% assign productos_categoria = productos_industria | where: "category", categoria %}
        {% for p in productos_categoria %}
        <article class="card">
          <a class="card-media" href="{{ p.url | relative_url }}">
            {% if p.image %}
            <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
            {% endif %}
          </a>
          <div class="card-body">
            <h3 class="card-title"><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
            {% if p.summary %}<p class="card-text">{{ p.summary }}</p>{% endif %}
            <a class="button" href="{{ p.url | relative_url }}">Ver detalles</a>
          </div>
        </article>
        {% endfor %}
      </div>
    {% endfor %}
  </section>
  <hr style="margin:32px 0">
{% endfor %}
