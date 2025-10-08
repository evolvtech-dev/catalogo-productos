---
layout: default
title: "Inicio"
---

<!-- HERO PRINCIPAL -->
<section class="hero">
  <h1>Comercializadora de Plásticos Potosina</h1>
  <p class="lead">Catálogo informativo de soluciones y productos plásticos con fichas técnicas e imágenes.</p>
</section>

<!-- SECCIÓN DE PRODUCTOS -->
<section id="productos">
  <h2>Productos</h2>
  <div class="grid">
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
        <a class="button" href="{{ p.url | relative_url }}">Ver detalles</a>
      </div>
    </article>
    {% endfor %}
  </div>
</section>

<!-- SECCIÓN DE MARCAS -->
<hr style="border:0;border-top:1px solid var(--border);margin:28px 0">

<section id="marcas">
  <h2>Marcas que distribuimos</h2>
  <p class="lead">Trabajamos con fabricantes líderes para garantizar calidad, disponibilidad y respaldo técnico.</p>

  <div class="brand-grid" style="display:grid;grid-template-columns:repeat(auto-fill,minmax(160px,1fr));gap:16px;align-items:center">
    <div class="brand-card"><img alt="Oatey" src="{{ '/assets/images/marcas/oatey.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="Spears" src="{{ '/assets/images/marcas/spears.jpg' | relative_url }}"></div>
    <div class="brand-card"><img alt="Cepex" src="{{ '/assets/images/marcas/cepex.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="GF" src="{{ '/assets/images/marcas/gf.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="Garlock" src="{{ '/assets/images/marcas/garlock.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="PCP" src="{{ '/assets/images/marcas/pcp.webp' | relative_url }}"></div>
    <div class="brand-card"><img alt="Tecno Plastic" src="{{ '/assets/images/marcas/tecno-plastic.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="Serrot" src="{{ '/assets/images/marcas/serrot.jpg' | relative_url }}"></div>
  </div>
</section>

<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section id="beneficios">
  <h2>¿Por qué elegir Comercializadora de Plásticos Potosina?</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:24px;margin-top:16px">
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Amplio catálogo</h3>
      <p>Ofrecemos soluciones plásticas de marcas líderes en el mercado, con disponibilidad inmediata.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Asesoría técnica</h3>
      <p>Nuestro equipo te ayuda a elegir el producto correcto según tu aplicación y requerimiento industrial.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Experiencia comprobada</h3>
      <p>Más de 15 años de trayectoria atendiendo a los sectores industrial, agrícola, minero y de construcción.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Envíos a todo México</h3>
      <p>Contamos con logística nacional y alianzas para entregas rápidas y seguras.</p>
    </div>
  </div>
</section>

<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section id="aplicaciones">
  <h2>Aplicaciones</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:24px;margin-top:16px">
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Agua y saneamiento</h3>
      <p>Sistemas de conducción de agua, drenaje, riego agrícola y plantas de tratamiento.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Química e industrial</h3>
      <p>Procesos químicos, manejo de fluidos corrosivos y líneas de producción.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Construcción</h3>
      <p>Instalaciones hidráulicas y sanitarias con materiales certificados de alta durabilidad.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Minería y energía</h3>
      <p>Aplicaciones en drenaje de químicos, floculación y conducción de agua en minería.</p>
    </div>
  </div>
</section>

<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section id="testimonios">
  <h2>Nuestros clientes opinan</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:24px;margin-top:16px">
    <blockquote style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <p>“Siempre recibimos asesoría técnica rápida y productos en tiempo. ¡Un excelente servicio!”</p>
      <footer style="color:var(--muted)">— Cliente industrial, Querétaro</footer>
    </blockquote>
    <blockquote style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <p>“Material de primera calidad. Hemos sustituido tuberías metálicas por plásticas con excelentes resultados.”</p>
      <footer style="color:var(--muted)">— Proveedor de construcción</footer>
    </blockquote>
  </div>
</section>


<!-- CTA FINAL -->
<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section id="contacto" class="cta" style="padding:24px;border:1px solid var(--border);border-radius:18px;background:linear-gradient(135deg,var(--brand),var(--brand-2));color:#0b0f19">
  <h2 style="margin:0 0 8px">Contáctanos</h2>
  <p style="margin:0 0 12px">Estamos listos para asesorarte y brindarte una cotización personalizada.</p>
  
  <div style="display:flex;flex-direction:column;gap:8px;margin-bottom:16px">
    <p style="margin:0;font-size:1.05rem"><strong>Teléfono:</strong> <a href="tel:4444594310" style="color:#0b0f19">444 459 4310</a></p>
    <p style="margin:0;font-size:1.05rem"><strong>WhatsApp:</strong> <a href="https://wa.me/524447142939" target="_blank" rel="noopener" style="color:#0b0f19">444 714 2939</a></p>
    <p style="margin:0;font-size:1.05rem"><strong>Correo:</strong> <a href="mailto:ventas@ctpslp.com.mx" style="color:#0b0f19">ventas@ctpslp.com.mx</a></p>
  </div>

  <div style="display:flex;gap:12px;flex-wrap:wrap">
    <a class="button" href="mailto:ventas@ctpslp.com.mx?subject=Cotización%20Catálogo%20CTP">Enviar correo</a>
    <a class="button" href="https://wa.me/524447142939" target="_blank" rel="noopener">Chatear por WhatsApp</a>
  </div>
</section>

