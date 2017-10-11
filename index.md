---
title: Home
---

If you're wondering what the heck this is all about then check out the [About page](/about.html). Otherwise we'll get straight to the posts.

---

{% for post in site.posts %}

# [{{ post.title }}]({{ post.url }})
{{ post.excerpt }}

---

{% endfor %}