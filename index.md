---
layout: default
title: think.ai - Quantum Physics Research Blog
---

<main class="page">

  <!-- HERO / INTRO -->
  <section class="hero" style="background-image: url('{{ "/IMG_5335.jpeg" | relative_url }}'); background-size: cover; background-position: center; min-height: 70vh; display: flex; align-items: center; justify-content: center; text-align: center; color: white;">
    <div>
      <p>Quantum Physics Research Blog</p>
      <h1>think.ai</h1>
      <p>Exploring the frontiers of theoretical physics — quantum mechanics, quantum field theory, attosecond physics, and mathematical methods.</p>
    
    </div>
  </section>


  <!-- Latest Posts -->
  <section id="latest-posts">
    <h2>Latest Posts</h2>
    <p>Check out the latest research notes and insights below.</p>
    {% for post in site.posts limit: 6 %}
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
    {% endfor %}
  </section>

</main>
