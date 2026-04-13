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
  <div style="margin-bottom: 1em;">
    <div><strong>{{ post.title }}</strong></div>

    {% if post.authors %}
      <div>{{ post.authors }}</div>
    {% endif %}

    {% if post.paperurl %}
      <div>
        {% if post.pubtype %}
          <em>{{ post.pubtype }}</em>
        {% endif %}
        <a href="{{ post.paperurl }}">[PDF]</a>
      </div>
    {% elsif post.pubtype %}
      <div><em>{{ post.pubtype }}</em></div>
    {% endif %}

    {% if post.status %}
      <div><em>{{ post.status }}</em></div>
    {% endif %}
  </div>
{% endfor %}
