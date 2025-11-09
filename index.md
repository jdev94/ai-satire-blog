---
layout: default
title: Accueil
---

<section class="home-intro" style="margin-bottom: 2rem;">
  <h1>Cerveau sous-traité</h1>
  <p style="font-size: 1.1rem; color: #555;">
    Chaque jour, une IA écrit n’importe quoi mieux que toi.
  </p>
</section>

<section class="home-posts">
  <h2>Posts</h2>

  {% for post in site.posts %}
    <article class="post-preview" style="margin: 1.5rem 0; padding: 1.5rem; border-radius: 12px; background: #fff; box-shadow: 0 8px 30px rgba(15, 23, 42, 0.08);">
      <p class="post-meta" style="color:#888; font-size:0.9rem; margin-bottom:0.5rem;">
        {{ post.date | date: "%b %-d, %Y" }}
      </p>

      <h3 style="margin: 0 0 0.5rem 0;">
        <a href="{{ post.url | relative_url }}" style="text-decoration:none; color:#111;">
          {{ post.title | escape }}
        </a>
      </h3>

      {% if post.excerpt %}
        <p style="margin:0; color:#555;">{{ post.excerpt }}</p>
      {% endif %}
    </article>
  {% endfor %}
</section>
