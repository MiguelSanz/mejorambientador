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
        <article class="art-cuadro">
          <h4><a href="{{ aroma.url }}">{{ aroma.nombre }}</a></h4>
          {% if aroma.imagen_cabecera %}
            <a href="{{ aroma.url }}"><img src="{{ aroma.imagen_cabecera}}" width="200" height="100" alt="{{ aroma.nombre }}"></a>
          {% else %}
            <p>(sin imagen)</p>
          {% endif %}          
          <p>Propiedades: {{ aroma.propiedades }}</p>
        </article>
    {% endfor %}
</section>


<!--
<ul>
    {% for aroma in site.aromas %}
        <li>
            <h2><a href="{{ aroma.url }}">{{ aroma.nombre }}</a></h2>
            <h3>{{ aroma.propiedades }}</h3>
            <p> {{ aroma.content | markdownify }}</p>
        </li>
    {% endfor %}
</ul>

<p>Prueba tags:</p>
{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

<p>Prueba categorías:</p>
{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
-->