---
layout: archive
title: Working Papers
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
You can also find my articles on my Google Scholar profile.
{% endif %}

{% include base_path %}

{% assign working = site.publications | where: "venue", "Working Papers" | sort: "date" | reverse %}

{% for post in working %}
  <p>
    <strong>{{ post.title }}</strong>
    {% if post.pubtype %}
      — <em>{{ post.pubtype }}</em>
    {% endif %}
    {% if post.paperurl %}
      <a href="{{ post.paperurl }}">[PDF]</a>
    {% endif %}<br>

    {% if post.authors %}
      {{ post.authors }}<br>
    {% endif %}

    {% if post.status %}
      <em>{{ post.status }}</em>
    {% endif %}
  </p>
{% endfor %}
