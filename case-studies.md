---
layout: default
title: case studies
permalink: /case-studies/
last_modified_at: 2021-07-30
---

<h1>Case Studies</h1>

{% assign case_studies = site.case_studies | sort:date | reverse %}
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
        <strong>Approach</strong>:&nbsp;
        {%- assign skills = case_study.skills | split:", " -%}
        {%- for skill in skills -%}
          <mark>
            {{ skill }}
          </mark>{% if forloop.last == false %},&nbsp;{% endif %}
        {%- endfor -%}
      </p>

      <p>
        <strong>Impact</strong>:
        {{ case_study.overview }}
        <a href="{{ case_study.url | relative_url }}">
          See how&thinsp;&rarr;
        </a>
      </p>

    </section>

  </article>

{% endfor %}
