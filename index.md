---
title: Homepage
header: Homepage
description: The homepage of Justin Croser.
permalink: /
layout: default
---

{% for post in site.posts %}
  <p class="blog-item"><b><a href="{{ post.url }}">{{ post.title }}</a></b><br>
  <span class="post-description">{{ post.description }}</span><br>
  <span class="post-meta">📅 {{ post.date | date_to_string }}</span></p>
{% endfor %}

<!-- **THESE LINKS ARE HIDDEN ON THE FRONT END** - they're only used for Mastodon verification purposes -->
<div class="verification-links">
  <a rel="me" href="https://fosstodon.org/@justincroser">Mastodon</a>
</div>
