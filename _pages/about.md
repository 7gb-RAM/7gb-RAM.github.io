---
layout: about
title: about
permalink: /
subtitle: M.S. Computer Science, <a href='https://www.montclair.edu/'>Montclair State University</a>

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>School of Computing</p>
    <p>Montclair State University</p>
    <p><a href="mailto:dasariv1@montclair.edu">dasariv1@montclair.edu</a></p>

selected_papers: false # the full publication list is rendered in the page body below
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # news is rendered in the page body below (after publications and projects)
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
---

I am a graduate researcher in Computer Science at Montclair State University, where I held a Graduate Assistantship from 2024 to 2026. My research focuses on making machine learning systems reliable enough for high-stakes settings, particularly clinical decision support. In the Software Systems Lab with Dr. Vaibhav Anu, I designed MAUQ-CLIP, a black-box uncertainty quantification framework for clinical large language models that treats missing evidence as an uncertainty signal. In the Data Science Lab with Dr. Hao Liu, I work on ontology-based clinical hallucination detection: verifying the clinical claims an LLM makes against a clinical ontology, and only trusting that check where the ontology actually covers the claim. My part of this work focuses on rigorous evaluation, including a held-out contamination experiment that separates genuine reasoning gains from retrieval of the answer key. Earlier, I co-developed GANterpolate, a hybrid GAN and interpolation framework for reconstructing sparse scientific data, which received the Best Paper Award at IEEE UEMCON 2025.

Before graduate school, I worked as a software developer at ADP, building internal platforms with React, Java, Spring Boot and Kafka. I received my B.Tech. in Electronics and Communication Engineering from Aditya University, India.

#### Research Interests

- Uncertainty quantification
- AI for healthcare
- Generative adversarial networks
- Graph neural networks
- Split learning

Outside of research, I enjoy music and chess.

<h2><a href="{{ '/publications/' | relative_url }}" style="color: inherit">selected publications</a></h2>

<div class="publications">
{% bibliography --query @*[selected=true]* %}
</div>

<h2><a href="{{ '/projects/' | relative_url }}" style="color: inherit">featured projects</a></h2>

{% assign featured_projects = site.projects | where: "featured", true | sort: "importance" %}

<div class="projects">
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in featured_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>

<h2><a href="{{ '/news/' | relative_url }}" style="color: inherit">announcements</a></h2>

{% include news.liquid limit=true %}

<!-- Hide Altmetric badges that have no recorded attention (score 0) -->
<style>
  .altmetric-embed:has(a[style*="/0.png"]) {
    display: none !important;
  }
</style>
