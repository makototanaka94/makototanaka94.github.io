---
layout: archive
title: Research
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
You can also find my articles on my Google Scholar profile.
{% endif %}

{% include base_path %}

<h2>Working Papers</h2>

{% assign working = site.publications | where: "venue", "Working Papers" | sort: "date" | reverse %}

{% for post in working %}
  <p>
    <strong>{{ post.title }}</strong><br>

    {% if post.authors %}
      {{ post.authors }}<br>
    {% endif %}

    {% if post.pubtype %}
      <em>{{ post.pubtype }}</em>
    {% endif %}
    {% if post.paperurl %}
      <a href="{{ post.paperurl }}">[PDF]</a>
    {% endif %}

    {% if post.status %}
      <br><em>{{ post.status }}</em>
    {% endif %}
  </p>
{% endfor %}

<hr>

<h2>Work in Progress</h2>

{% assign wip = site.publications | where: "venue", "Work in Progress" | sort: "date" | reverse %}

{% for post in wip %}
  <p>
    <strong>{{ post.title }}</strong><br>

    {% if post.authors %}
      {{ post.authors }}<br>
    {% endif %}

    {% if post.status %}
      <em>{{ post.status }}</em>
    {% endif %}
  </p>
{% endfor %}
