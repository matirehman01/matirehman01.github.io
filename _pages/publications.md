---
layout: default
title: "Research: AI Contestation and Attribution"
permalink: /publications/
excerpt: "Research and publications by Mati Ur Rehman on AI contestation, attribution, AI blaming, and human responses to automated decisions."
---

{% include base_path %}
{% assign publications = site.publications | sort: "date" | reverse %}

<main class="notebook-home notebook-research" aria-labelledby="research-title">
  <section class="notebook-research-hero">
    <div>
      <p class="notebook-kicker">Research</p>
      <h1 id="research-title">Research and publications</h1>
      <p class="notebook-dek">Current work on AI contestation, attribution, AI blaming, and human responses to automated decisions.</p>
    </div>

    <aside class="research-summary research-summary--compact">
      <p class="notebook-section-label">Current focus</p>
      <p>AI Contestation, Attribution, AI Blaming.</p>
    </aside>

    <div class="notebook-actions" aria-label="Research links">
      {% if site.author.googlescholar %}
        <a class="notebook-button notebook-button--primary" href="{{ site.author.googlescholar }}"><i class="fas fa-graduation-cap" aria-hidden="true"></i> Google Scholar</a>
      {% endif %}
      <a class="notebook-button" href="/files/Mati_Ur%20Rehman-Curriculum_Vitae.pdf"><i class="fas fa-file-alt" aria-hidden="true"></i> Download CV</a>
      <a class="notebook-button" href="mailto:mati@iastate.edu"><i class="fas fa-envelope" aria-hidden="true"></i> Email</a>
    </div>
  </section>

  <section class="notebook-research-section" aria-labelledby="current-ai-work">
    <div class="notebook-research-heading">
      <p class="notebook-section-label">Current stream</p>
      <h2 id="current-ai-work">AI contestation, attribution, and AI blaming</h2>
    </div>

    <div class="notebook-publications">
      {% for post in publications %}
        {% if post.research_stream == "ai" %}
          <article class="notebook-publication" itemscope itemtype="https://schema.org/CreativeWork">
            <div class="notebook-publication__meta">
              <span>{{ post.date | default: "1900-01-01" | date: "%Y" }}</span>
              {% if post.venue %}
                <span>{{ post.venue }}</span>
              {% endif %}
            </div>

            <h3 itemprop="headline">
              <a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>
            </h3>

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
        {% endif %}
      {% endfor %}
    </div>
  </section>

  <section class="notebook-research-section notebook-research-section--secondary" aria-labelledby="adjacent-work">
    <div class="notebook-research-heading">
      <p class="notebook-section-label">Earlier / adjacent work</p>
      <h2 id="adjacent-work">Platforms, social commerce, and digital affordances</h2>
    </div>

    <div class="notebook-publications notebook-publications--secondary">
      {% for post in publications %}
        {% if post.research_stream == "platforms" %}
          <article class="notebook-publication" itemscope itemtype="https://schema.org/CreativeWork">
            <div class="notebook-publication__meta">
              <span>{{ post.date | default: "1900-01-01" | date: "%Y" }}</span>
              {% if post.venue %}
                <span>{{ post.venue }}</span>
              {% endif %}
            </div>

            <h3 itemprop="headline">
              <a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>
            </h3>

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
        {% endif %}
      {% endfor %}
    </div>
  </section>
</main>
