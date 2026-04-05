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
    <strong>{{ post.title }}</strong><br>
    {{ post.authors }}<br>
    <em>{{ post.pubtype }}</em>
    {% if post.paperurl %} [PDF]{% endif %}
  </p>
{% endfor %}
