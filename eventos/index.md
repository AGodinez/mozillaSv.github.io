---
layout: page
title: "Eventos"
date:  
modified:
excerpt: "Proximos eventos de Mozilla El Salvador"
image:
  feature:
---

<ul class="post-list">
{% if site.categories.eventos %}
  {% for post in site.categories.eventos %}
    <li>
      <article>
        <a href="{{ site.url }}{{ post.url }}">
          {{ post.title }}
          <span class="entry-date">
            <time datetime="{{ post.date | date_to_xmlschema }}">
              {{ post.date | date: "%B %d, %Y" }}
            </time>
          </span>
          {% if post.excerpt %}
          <span class="excerpt">{{ post.excerpt }}</span>
          {% endif %}
        </a>
      </article>
    </li>
  {% endfor %}
{% else %}
  <div class="no-posts">
    <h4>Lo sentimos! No hay eventos que mostrar.</h4>
  </div>
{% endif %}
</ul>
