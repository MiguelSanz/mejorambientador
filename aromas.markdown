---
layout: page
title: Aromas
permalink: /aromas/
sitemap:
  priority: 0.8
  changefreq: 'weekly'
---
<section class="seccion"> 
    {% for aroma in site.aromas %}
    {% capture tmp_url %}{{ aroma.url }}{% endcapture %}
    {% capture tmp_url_texto %}{{ aroma.nombre }}{% endcapture %}
    {% capture tmp_imagen %}{{ aroma.imagen_cabecera }}{% endcapture %}
    {% capture tmp_alt %}{{ aroma.nombre }}{% endcapture %}
    {% capture tmp_extracto %}{{ aroma.extracto }}{% endcapture %}
    {% include articulo.html 
       url=tmp_url
       url_texto=tmp_url_texto
       imagen=tmp_imagen
       alt=tmp_alt
       max-width="200px"
       extracto=tmp_extracto %}
    {% endfor %}
</section>