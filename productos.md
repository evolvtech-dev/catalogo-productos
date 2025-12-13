---
layout: default
title: "Productos"
permalink: /productos/
---

<!-- HERO PRINCIPAL -->
<section class="hero">
  <h1>Catálogo de productos</h1>
  <p class="lead">Explora nuestras soluciones plásticas por categoría. Usa los filtros para encontrar lo que necesitas rápidamente.</p>
</section>

<!-- FILTROS -->
<section style="margin-bottom:28px">
  <h2>Filtrar por categoría</h2>
  <div id="filtros" style="display:flex;flex-wrap:wrap;gap:12px;margin-top:12px">
    <button class="filtro-btn is-active" data-filtro="todos">Todos</button>
    <button class="filtro-btn" data-filtro="tuberia">Tubería</button>
    <button class="filtro-btn" data-filtro="conexiones">Conexiones</button>
    <button class="filtro-btn" data-filtro="valvulas">Válvulas</button>
    <button class="filtro-btn" data-filtro="adhesivos">Cementos y adhesivos</button>
    <button class="filtro-btn" data-filtro="bombas">Equipos de bombeo</button>
    <button class="filtro-btn" data-filtro="tinacos">Tinacos</button>
    <button class="filtro-btn" data-filtro="otros">Otros</button>
  </div>
</section>

<!-- GRID DE PRODUCTOS -->
<section class="grid" id="productos-lista">
  {% assign productos = site.products | sort: 'order' %}
  {% for p in productos %}
    <article class="card filtro-item" data-categoria="{{ p.category | slugify }}">
      <a class="card-media" href="{{ p.url | relative_url }}">
        {% if p.image %}
          <img src="{{ p.image | relative_url }}" alt="{{ p.title }}" loading="lazy">
        {% endif %}
      </a>
      <div class="card-body">
        <h3 class="card-title"><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
        {% if p.summary %}<p class="card-text">{{ p.summary }}</p>{% endif %}
        <a class="button" href="{{ p.url | relative_url }}">Ver detalles</a>
      </div>
    </article>
  {% endfor %}
</section>

<!-- SCRIPT DE FILTRO -->
<script>
  const botones = document.querySelectorAll('.filtro-btn');
  const items = document.querySelectorAll('.filtro-item');

  botones.forEach(btn => {
    btn.addEventListener('click', () => {
      botones.forEach(b => b.classList.remove('is-active'));
      btn.classList.add('is-active');
      const filtro = btn.dataset.filtro;

      items.forEach(item => {
        const cat = item.dataset.categoria;
        if (filtro === 'todos' || cat === filtro) {
          item.style.display = '';
        } else {
          item.style.display = 'none';
        }
      });
    });
  });
</script>
