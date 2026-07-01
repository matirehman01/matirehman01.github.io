---
layout: default
title: "Research and Publications"
permalink: /publications/
excerpt: "Research and publications by Mati Ur Rehman on AI contestation, explainable AI, accountability, and human responses to automated decisions."
---

{% include base_path %}

<main class="notebook-home notebook-research" aria-labelledby="research-title">
  <section class="notebook-research-hero">
    <p class="notebook-kicker">Research</p>
    <h1 id="research-title">Research and publications</h1>
    <p class="notebook-dek">Current work on AI contestation, explainable AI, accountability, and human responses to automated decisions.</p>

    <div class="notebook-actions" aria-label="Research links">
      {% if site.author.googlescholar %}
        <a class="notebook-button notebook-button--primary" href="{{ site.author.googlescholar }}">Google Scholar</a>
      {% endif %}
      <a class="notebook-button" href="/files/Mati_Ur Rehman-Curriculum_Vitae.pdf">Download CV</a>
      <a class="notebook-button" href="mailto:mati@iastate.edu">Email</a>
    </div>
  </section>

  <section class="notebook-research-layout" aria-label="Publication list">
    <aside class="notebook-research-note">
      <p class="notebook-section-label">Current focus</p>
      <p>AI contestability, explainable AI, responsibility attribution, and organizational responses to AI-mediated decisions.</p>
    </aside>

    <div class="notebook-publications">
      {% assign publications = site.publications | sort: "date" | reverse %}
      {% for post in publications %}
        <article class="notebook-publication" itemscope itemtype="https://schema.org/CreativeWork">
          <div class="notebook-publication__meta">
            <span>{{ post.date | default: "1900-01-01" | date: "%Y" }}</span>
            {% if post.venue %}
              <span>{{ post.venue }}</span>
            {% endif %}
          </div>

          <h2 itemprop="headline">
            <a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>
          </h2>

          {% if post.citation %}
            <p>{{ post.citation }}</p>
          {% endif %}

          <div class="notebook-publication__links">
            <a href="{{ base_path }}{{ post.url }}">Details</a>
            {% if post.paperurl %}
              <a href="{{ post.paperurl }}">Paper</a>
            {% endif %}
          </div>
        </article>
      {% endfor %}
    </div>
  </section>
</main>
