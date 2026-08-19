---
# the default layout is 'page'
layout: page
title: Home
permalink: /
---

![Puzzle Wizards Banner](assets/img/pw_banner.jpg)

Welcome to my puzzle wizards wiki where you can find useful information on several aspects of the game!

I wanted to create a knowledge base after learning tips and tricks as a new player.
Hopefully you find this guide useful and go support the devs by downloading and playing the game on mobile/Steam at [Puzzle Wizards](https://puzzlewizards.net/)!

You can find posts by going to the categories tab in the sidebar or by going through the tags.

## Recommended Posts:

<div class="suggested-posts">
  {% assign suggested_paths = "_posts/2026-08-09-home.md|_posts/2026-08-09-guilds.md|" | split: "|" %}
  {% for path in suggested_paths %}
    {% assign post = site.posts | where: "path", path | first %}
    {% if post %}
    <a class="suggested-post-card" href="{{ post.url | relative_url }}">
      <span class="suggested-post-title">{{ post.title }}</span>
      {% if post.description %}
      <span class="suggested-post-desc">{{ post.description }}</span>
      {% endif %}
    </a>
    {% endif %}
  {% endfor %}
</div>
