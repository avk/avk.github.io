---
layout: default
title: Contact
permalink: /contact/
---

<img src="{{ site.url }}/assets/contact.png" alt="Let's get the gears rolling" style="float: right; margin: 0 0 100px 20px;" />

# Contact 

> As of May 2017, I'm looking for full-time work.

{% include goal.md %}

{% if site.social.email %}
  <h2>
    <a href="mailto:{{ site.social.email }}" title="Email">
      <span class="icon icon-at"></span>
      {{ site.social.email }}
    </a>
  </h2>
{% endif %}
{% if site.social.linkedin %}
  <h2>
    <a href="https://www.linkedin.com/in/{{ site.social.linkedin }}" target="_blank" title="LinkedIn">
      <span class="icon icon-social-linkedin"></span>
      LinkedIn
    </a>
  </h2>
{% endif %}
{% if site.social.github %}
  <h2>
    <a href="https://github.com/{{ site.social.github }}" target="_blank" title="GitHub">
      <span class="icon icon-social-github"></span>
      GitHub
    </a>
  </h2>
{% endif %}
{% if site.social.twitter %}
  <h2>
    <a href="https://twitter.com/{{ site.social.twitter }}" target="_blank" title="Twitter">
      <span class="icon icon-social-twitter"></span>
      Twitter
    </a>
  </h2>
{% endif %}

