---
layout: page
permalink: /publications/
title: publications
description: an up-to-date list is also available on Google Scholar
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->
{% include bib_search.liquid %}

<div class="publications">

{% capture preprints %}
  {% bibliography -f papers -q @unpublished %}
{% endcapture %}
{% assign preprints_stripped = preprints | strip %}
{% if preprints_stripped contains '<li>' %}
  <h1 class="category">Preprints</h1>
  {{ preprints }}
{% endif %}

{% capture articles %}
  {% bibliography -f papers -q @article %}
{% endcapture %}
{% assign articles_stripped = articles | strip %}
{% if articles_stripped contains '<li>' %}
  <h1 class="category">Journal articles</h1>
  {{ articles }}
{% endif %}

</div>

