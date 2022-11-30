---
layout: page
title: Home
id: home
permalink: /
---

# Hi there!

I just found out about [digital gardening](https://maggieappleton.com/garden-history), and wanted to try it out. Let's see how this goes?

Here's a list of notes so far:

<ul class="post-list">
  {% for note in site.notes %}
    <li>
      <a href="{{ note.url }}" class="internal-link">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>