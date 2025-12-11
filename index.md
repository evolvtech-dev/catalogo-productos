---
layout: default
title: "Inicio"
---

<!-- HERO PRINCIPAL -->
<section class="hero">
  <h1>Comercializadora de Plásticos Potosina</h1>
  <p class="lead">Soluciones plásticas industriales con respaldo técnico, fichas informativas y atención personalizada.</p>
</section>

<!-- CATEGORÍAS POR INDUSTRIA -->
<section id="sectores" style="margin-top:48px">
  <h2>Explora por sector</h2>
  <div class="grid">
    <a class="card" href="{{ '/mercado/edificacion/' | relative_url }}">
      <div class="card-media"><img src="{{ '/assets/images/sectores/edificacion.jpg' | relative_url }}" alt="Edificación"></div>
      <div class="card-body">
        <h3 class="card-title">Edificación</h3>
        <p class="card-text">Materiales para instalaciones hidráulicas y sanitarias en obra civil y residencial.</p>
      </div>
    </a>
    <a class="card" href="{{ '/mercado/infraestructura/' | relative_url }}">
      <div class="card-media"><img src="{{ '/assets/images/sectores/infraestructura.jpg' | relative_url }}" alt="Infraestructura"></div>
      <div class="card-body">
        <h3 class="card-title">Infraestructura</h3>
        <p class="card-text">Soluciones para redes de agua potable, drenaje, alcantarillado y urbanización.</p>
      </div>
    </a>
    <a class="card" href="{{ '/mercado/industria/' | relative_url }}">
      <div class="card-media"><img src="{{ '/assets/images/sectores/industria.jpg' | relative_url }}" alt="Industria"></div>
      <div class="card-body">
        <h3 class="card-title">Industria</h3>
        <p class="card-text">Tubería, conexiones y válvulas para procesos químicos, alimentarios y productivos.</p>
      </div>
    </a>
  </div>
</section>

<!-- BENEFICIOS -->
<hr style="border:0;border-top:1px solid var(--border);margin:48px 0">
<section id="beneficios">
  <h2>¿Por qué elegirnos?</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:24px;margin-top:16px">
    <div class="card"><div class="card-body">
      <h3 class="card-title">Envíos a todo México</h3>
      <p class="card-text">Contamos con cobertura nacional y logística confiable.</p>
    </div></div>
    <div class="card"><div class="card-body">
      <h3 class="card-title">Asesoría técnica</h3>
      <p class="card-text">Ingenieros listos para ayudarte a elegir el producto ideal.</p>
    </div></div>
    <div class="card"><div class="card-body">
      <h3 class="card-title">Stock disponible</h3>
      <p class="card-text">Entrega rápida de líneas seleccionadas en inventario.</p>
    </div></div>
    <div class="card"><div class="card-body">
      <h3 class="card-title">15+ años de experiencia</h3>
      <p class="card-text">Respaldo sólido atendiendo industrias, construcción y más.</p>
    </div></div>
  </div>
</section>

<!-- MARCAS -->
<hr style="border:0;border-top:1px solid var(--border);margin:48px 0">
<section class="brands" aria-labelledby="marcas">
  <h2 id="marcas">Marcas que distribuimos</h2>
  <p class="lead">Trabajamos con fabricantes líderes para garantizar calidad, disponibilidad y respaldo técnico.</p>
  <div class="brands-grid">
    {% assign logos = "OATEY LOGO.png,LOGO SPEARS COLOR 4.6X4 CMC..jpg,CEPEX LOGO.png,GF.png,GARLOCK LOGO.png,PCP LOGO.webp,TECNO PLASTIC LOGO.png,LOGO SERROT 10X4 CMS. COLOR.jpg" | split: "," %}
    {% for logo in logos %}
      <div class="brand-card">
        <img src="{{ '/assets/images/marcas/' | append: logo | relative_url }}" alt="Marca {{ forloop.index }}">
      </div>
    {% endfor %}
  </div>
</section>

<!-- TESTIMONIOS -->
<hr style="border:0;border-top:1px solid var(--border);margin:48px 0">
<section id="testimonios">
  <h2>Lo que opinan nuestros clientes</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:24px;margin-top:16px">
    <blockquote class="card"><div class="card-body">
      <p>“Su asesoría fue clave para especificar productos en una planta industrial. Muy profesionales.”</p>
      <footer style="color:var(--muted)">— Ingeniero de proyecto, Querétaro</footer>
    </div></blockquote>
    <blockquote class="card"><div class="card-body">
      <p>“Hemos recibido pedidos a tiempo con excelente calidad. Seguiremos trabajando con CTP.”</p>
      <footer style="color:var(--muted)">— Compras, desarrolladora residencial</footer>
    </div></blockquote>
  </div>
</section>

<!-- CTA FINAL -->
<hr style="border:0;border-top:1px solid var(--border);margin:48px 0">
<section id="contacto" class="cta cta--pro">
  <h2>¿Requieres una cotización?</h2>
  <p class="lead" style="margin-bottom:18px">Nuestro equipo puede ayudarte a encontrar el producto exacto para tu necesidad.</p>
  <div style="display:flex;gap:12px;flex-wrap:wrap">
    <a class="button" href="mailto:ventas@ctpslp.com.mx">Enviar correo</a>
    <a class="button" href="https://wa.me/524447142939" target="_blank" rel="noopener">Chatear por WhatsApp</a>
    <a class="button" href="tel:4444594310">Llamar ahora</a>
  </div>
</section>
