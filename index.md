---
layout: default
title: think.ai - Quantum Physics Research Blog
---

<div class="home">
  <p class="post-meta">Quantum Physics Research Blog</p>
  <h1 class="page-heading">think.ai</h1>
  <p>Exploring the frontiers of theoretical physics — quantum mechanics, quantum field theory, attosecond physics, and mathematical methods.</p>

  <section id="latest-posts" style="margin-top: 60px;">
    <h2>Latest Posts</h2>
    <p class="post-meta">Check out the latest research notes and insights below.</p>
    {% for post in site.posts limit: 6 %}
      <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% endfor %}
            <a class="post-link" href="{{ '/equations' | relative_url }}">Showcase of Fundamental Equations</a>
  </section>
</div>
