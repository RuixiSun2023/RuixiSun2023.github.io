---
layout: default
title: About
permalink: /
subtitle: Photoacoustic & Ultrasound Imaging | Signal Processing | FPGA Systems
stylesheet: /assets/css/home.css
selected_papers: true
---

<div class="post home-page">
  <header class="post-header">
    <h1 class="post-title">{{ site.title }}</h1>
    <p class="desc">{{ page.subtitle }}</p>
  </header>

  <section class="home-introduction" aria-label="About Ruixi Sun">
    <div class="home-copy">
      <p class="home-lead">Hi, I’m Ruixi Sun! I work on photoacoustic and ultrasound imaging, with a particular interest in signal processing and real-time FPGA systems.</p>
      <p>I earned my M.S. at ShanghaiTech University, working with <a href="http://www.hislab.cn">Prof. Fei Gao</a> and <a href="https://suitlaboratory.github.io">Prof. Xiran Cai</a>. Before that, I studied Measurement and Control Technology and Instruments at North University of China.</p>
      <p>My labmates call me “Engineer Sun.” Alongside imaging algorithms and experiments, I maintain our lab’s servers and experimental equipment. I enjoy building things, figuring out why they don’t work, and turning ideas into working systems.</p>
      <p class="home-links"><a href="https://scholar.google.com/citations?user={{ site.data.socials.scholar_userid }}" target="_blank" rel="noopener noreferrer">Google Scholar ↗</a></p>
    </div>
    <figure class="home-portrait">
      {% include figure.liquid path="assets/img/ruixi-sun-profile.jpg" alt="Ruixi Sun outdoors beside a black swan" loading="eager" sizes="(max-width: 700px) calc(100vw - 44px), (max-width: 1160px) 34vw, 380px" %}
    </figure>
  </section>

  <section class="home-research" aria-labelledby="research-interests">
    <h2 id="research-interests">Research Interests</h2>
    <p class="home-section-intro">I want to build imaging systems that help doctors see more clearly, bringing together three closely connected areas.</p>
    <div class="home-research-grid">
      <section class="home-research-item" aria-labelledby="research-imaging">
        <h3 id="research-imaging">Photoacoustic &amp; Ultrasound Imaging</h3>
        <p>I explore ways to use photoacoustic and ultrasound imaging to reveal details that conventional imaging might miss.</p>
      </section>
      <section class="home-research-item" aria-labelledby="research-signals">
        <h3 id="research-signals">Biomedical Signal Processing</h3>
        <p>A good image starts with good signals. I develop ways to reduce noise, remove artifacts, and recover information that might otherwise be lost.</p>
      </section>
      <section class="home-research-item" aria-labelledby="research-fpga">
        <h3 id="research-fpga">Real-Time FPGA Systems</h3>
        <p>I like seeing an algorithm run on real hardware. I use FPGAs to process imaging signals faster and bring imaging systems closer to real-time operation.</p>
      </section>
    </div>
  </section>

{% if page.selected_papers %}

  <section class="home-publications" aria-labelledby="selected-publications">
    <div class="home-section-heading">
      <h2 id="selected-publications">Selected Publications</h2>
      <a href="{{ '/publications/' | relative_url }}">All publications ↗</a>
    </div>
    {% include selected_papers.liquid %}
  </section>
  {% endif %}
</div>
