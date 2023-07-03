---
layout: page
permalink: /repositories/
title: repos
description: Olen koonnut tänne GitHubista käyttäjiä, organisaatiota ja repoja joita kannattaa seurata saavutettavuuden näkökulmasta. Mikäli sinulle tulee vastaan mielenkiintoisia käyttäjiä, organisaatiota tai repoja jotkoa voisi tänne lisätä niin kerrothan siitä minulle.
nav: true
nav_order: 3
---

## GitHub käyttäjät

{% if site.data.repositories.github_users %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.html username=user %}
  {% endfor %}
</div>

---


## GitHub Repot

{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
