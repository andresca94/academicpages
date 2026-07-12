---
permalink: /
title:
excerpt: "AI creative technologist focused on generative video, VFX-oriented AI workflows, prompt systems, and automation infrastructure for fashion, marketing, e-commerce, and social-first content teams."
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div class="creative-home">
  <section class="creative-home__hero creative-home__hero--dashboard">
    <div class="creative-home__hero-grid creative-home__hero-grid--compact">
      <div class="creative-home__hero-copy">
        <div class="creative-home__eyebrow">AI CREATIVE TECHNOLOGIST · VIDEO AI SYSTEMS · AUTOMATION</div>
        <h1 class="creative-home__headline">Building AI-native creative systems for fashion, media, and social-first brands.</h1>
        <p class="creative-home__lede creative-home__lede--compact">
          I build the layer between creative direction and technical execution: prompt systems, generative video,
          VFX-oriented AI workflows, automation, localization, and production infrastructure that helps teams move
          from brief to polished output faster without losing realism, taste, or scalability.
        </p>
        <ul class="creative-home__chips">
          <li>Fashion & luxury aesthetics</li>
          <li>Social-first video</li>
          <li>E-commerce creative</li>
          <li>Paid media variants</li>
          <li>AI avatars</li>
          <li>Creative automation</li>
          <li>Prompt systems</li>
          <li>VFX workflows</li>
          <li>Content localization</li>
        </ul>
      </div>
      <figure class="creative-home__portrait creative-home__portrait--compact">
        <img src="{{ '/images/andres-creative-profile.png' | relative_url }}" alt="Andres Carvajal portrait" />
      </figure>
    </div>

    <div class="creative-home__insight-panel">
      <div class="creative-home__insight-tabs" aria-label="Home summary views">
        <button type="button" class="creative-home__insight-tab is-active" data-home-panel-target="build">What I build</button>
        <button type="button" class="creative-home__insight-tab" data-home-panel-target="industries">Industries</button>
        <button type="button" class="creative-home__insight-tab" data-home-panel-target="stack">Stack</button>
      </div>

      <div class="creative-home__insight-panels">
        <section class="creative-home__summary-card is-active" data-home-panel="build">
          <div class="creative-home__card-label">What I build</div>
          <h2 class="creative-home__summary-title">Creative intelligence, video AI, and automation infrastructure.</h2>
          <p class="creative-home__summary-copy">
            Research, prompting, motion systems, localization, review workflows, and production automation designed to
            move from brief to polished output faster.
          </p>
        </section>

        <section class="creative-home__summary-card" data-home-panel="industries" hidden>
          <div class="creative-home__card-label">Best-fit industries</div>
          <h2 class="creative-home__summary-title">Fashion, beauty, media, and commerce.</h2>
          <p class="creative-home__summary-copy">
            Fashion, beauty & luxury, social media, digital marketing, paid media, brand campaigns, e-commerce,
            creator media, and editorial storytelling.
          </p>
        </section>

        <section class="creative-home__summary-card" data-home-panel="stack" hidden>
          <div class="creative-home__card-label">Creative + technical stack</div>
          <h2 class="creative-home__summary-title">Prompting, video AI, automation, and deployment.</h2>
          <p class="creative-home__summary-copy">
            Prompt engineering, ComfyUI, diffusion, AI video pipelines, avatars, n8n, FastAPI, Python, cloud
            deployment, and quality control loops. Broader LLM and full-stack AI work lives on my
            <a href="https://andresca94.github.io/">full portfolio</a>.
          </p>
        </section>
      </div>
    </div>
  </section>
</div>

<script>
  (function () {
    var root = document.querySelector(".creative-home");
    if (!root) return;

    var buttons = Array.prototype.slice.call(root.querySelectorAll("[data-home-panel-target]"));
    var panels = Array.prototype.slice.call(root.querySelectorAll("[data-home-panel]"));
    if (!buttons.length || !panels.length) return;

    function activateHomePanel(target) {
      buttons.forEach(function (button) {
        var isActive = button.getAttribute("data-home-panel-target") === target;
        button.classList.toggle("is-active", isActive);
        button.setAttribute("aria-pressed", isActive ? "true" : "false");
      });

      panels.forEach(function (panel) {
        var isActive = panel.getAttribute("data-home-panel") === target;
        panel.classList.toggle("is-active", isActive);
        panel.hidden = !isActive;
      });
    }

    buttons.forEach(function (button) {
      button.addEventListener("click", function () {
        activateHomePanel(button.getAttribute("data-home-panel-target"));
      });
    });

    activateHomePanel("build");
  })();
</script>
