---
text: "Posters"
layout: page
permalink: /publications/
title: Publications
description: All of my preprints, ideas, papers and posters.
nav: true
nav_order: 2
sortby: true # true: Sort by types | false: Sort by years
years: [2024, 2023, 2022, 2021]
sections:
  - bibquery: "@preprint"
    text: "Preprint articles"
  - bibquery: "@poster"
    text: "Posters"
  - bibquery: "@dataset"
    text: "Dataset"
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
