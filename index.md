---
title: Home
---

This is a blog where I talk about the crazy unique properties of Pokémon that you never noticed while playing the games. If you want to know more about this blog and me, check out the [About page](/about.html). Otherwise we'll get straight to the posts.

---

{% for post in site.posts %}

# [{{ post.title }}]({{ post.url }})
{{ post.excerpt }}

---

{% endfor %}