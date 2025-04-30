---
layout: page
permalink: /repositories/
title: featured repositories
description:
nav: false
nav_order: 4
---

For all project repositories, visit [https://github.com/eahowerton](https://github.com/eahowerton).

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
