---
layout: default
title: Artigo de opinião
permalink: /artigo_opiniao/
---

<h1 class="mb-4">Artigos de Opinião</h1>

{% for artigo in site.artigos %}
  <article class="mb-4">
    <h2>
      <a href="{{ artigo.url }}">{{ artigo.title }}</a>
    </h2>
    <p class="text-muted">
      {{ artigo.date | date: "%d %B %Y" }}
    </p>
    <p>
      {{ artigo.excerpt | strip_html | truncate: 160 }}
    </p>
    <a href="{{ artigo.url }}">Ler artigo</a>
  </article>
{% endfor %}
