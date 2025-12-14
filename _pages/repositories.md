---
layout: page
permalink: /repositories/
title: repositories
description: >
  Our group develops software and computational tools in paleogenomics and population genetics.
  Below we list the GitHub profiles of contributors, together with links to repositories hosting our
  various resources. Most of our code is freely accessible and released as open-source software.
  Unless stated otherwise, our software is distributed under the
  <a href="https://www.gnu.org/licenses/gpl-3.0.en.html" target="_blank" rel="noopener">
  GNU General Public License v3.0</a> and is provided <em>as is</em>, without any warranty.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
