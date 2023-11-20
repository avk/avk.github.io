---
layout: default
title: case studies
permalink: /case-studies/
last_modified_at: 2021-07-30
---

<h1>Case Studies</h1>

{% assign case_studies = site.case_studies | sort:date | reverse | where:
"active", true %}
{% for case_study in case_studies %}

  <article class="case_study">

    <a href="{{ case_study.url | relative_url }}">
      <img
        alt="Work sample from {{ case_study.title }}"
        class="cover"
        src="{{ site.url }}{{ case_study.cover_image }}"
      />
    </a>

    <section class="summary">

      <h2>
        <a href="{{ case_study.url | relative_url }}" title="{{ case_study.title }}">
          {{ case_study.title }}
        </a>
      </h2>

      <p>
        {{ case_study.overview }}
        <a href="{{ case_study.url | relative_url }}">
          See how&thinsp;&rarr;
        </a>
      </p>

    </section>

  </article>

{% endfor %}
