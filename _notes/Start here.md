---
title: Start here
share: true
---

I haven't decided what to include here just yet. So far I'm just building things, which I'll detail in [[About this site]].

Eventually I'll put a list of tags in here.

<h2>Tags</h2>
{% assign tags =  site.notes | map: 'tags' | uniq %}
{% for tag in tags %}
  <h3>{{ tag }}</h3>
  <ul>
  {% for note in site.notes %}
    {% if note.tags contains tag %}
    <li><a href="{{ site.baseurl }}{{ note.url }}" class="internal-link">{{ note.title }}</a></li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}

<h2>Categories</h2>
{% assign categories =  site.notes | map: 'categories' | uniq %}
{% for category in categories %}
  <h3>{{ category }}</h3>
  <ul>
  {% for note in site.notes %}
    {% if note.category contains category %}
    <li><a href="{{ site.baseurl }}{{ note.url }}" class="internal-link">{{ note.title }}</a></li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}
