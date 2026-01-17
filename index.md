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
      <a href="{{ "/blog/" | relative_url }}">Read the Blog</a>
    </div>
  </section>

  <!-- Research Focus -->
  <section id="research-focus">
    <h2>Research Focus</h2>
    <ul>
      <li><strong>Quantum Mechanics</strong>: Wave functions, operators, uncertainty, measurement, and structure of states.</li>
      <li><strong>Quantum Field Theory</strong>: Path integrals, Feynman diagrams, quantization, and symmetry principles.</li>
      <li><strong>Attosecond Physics</strong>: Ultrafast dynamics, strong-field interaction, and time-resolved spectroscopy.</li>
      <li><strong>Mathematical Physics</strong>: Symmetries, group theory, geometric methods, and functional analysis tools.</li>
      <li><strong>Computational Physics</strong>: Numerical methods, simulations, and reproducible computational notebooks.</li>
      <li><strong>Research Notes</strong>: Derivations, structured reading notes, and clean LaTeX-ready writeups.</li>
    </ul>
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
