---
text: "Posters"
layout: page
permalink: /publications/
title: Publications
description: 
nav: true
nav_order: 2
sortby: true        # true: Sort by types | false: Sort by years
years: [2024, 2023, 2022, 2021]
sections:
  - bibquery: "@preprint"
    text: "Preprint articles"
#   - bibquery: "@inproceedings"
#     text: "Conference and Workshop articles"
  - bibquery: "@poster"
    text: "Posters"
  - bibquery: "@data|@dataset"
    text: "Dataset"
---
<!-- _pages/publications.md -->

<div class="publications">

{%- if page.sortby -%}
{%- for section in page.sections %}
`<a id="{{section.text}}"></a>`

<p class="bibtitle">{{section.text}}</p>
{%- for y in page.years %}

    {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
            {%- capture citecount -%}
            {%- bibliography_count -f {{site.scholar.bibliography}} -q {{section.bibquery}}[year={{y}}] -%}
            {%- endcapture -%}

    {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
            {%- if citecount !="0" %}

    {% bibliography -f {{site.scholar.bibliography}} -q {{section.bibquery}}[year={{y}}] %}

    {%- endif -%}

    {%- endfor %}

    {%- endfor %}

{%- else -%}

    {% bibliography -f {{ site.scholar.bibliography }} %}

{%- endif -%}

</div>
