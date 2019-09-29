---
layout: archive
title: "Publications"
permalink: /paper_summaries/
author_profile: false
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.paper_summary %}
  {% include archive-single.html %}
{% endfor %}
