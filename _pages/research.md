---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 1
description: 
redirect_from:
  - /projects/
---

My current is on water infrastructure condition, performance, and affordability.

{% assign selected = site.projects | sort: 'importance' %}
{% for project in selected %}{% include research-row.liquid project=project %}{% endfor %}

## Some work in progress

See the [publications page]({{ '/publications/' | relative_url }}) for conference contributions and manuscripts under review.
