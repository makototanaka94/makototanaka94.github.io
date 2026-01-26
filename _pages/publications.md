---
layout: archive
title: "Working Papers"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% assign working = site.publications | where: "venue", "Working Papers" | sort: "date" | reverse %}

{% for post in working %}
  <p>
    <strong>{{ post.title }}</strong>
    {% if post.paperurl %}
      &nbsp;[<a href="{{ post.paperurl | relative_url }}">PDF</a>]
    {% endif %}
  </p>
{% endfor %}


<!-- <br/> -->
