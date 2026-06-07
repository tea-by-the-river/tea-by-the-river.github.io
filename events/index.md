---
layout: page
title: Events
---

{% assign events = site.pages | where: "layout", "event" | sort: "date" | reverse %}
{% if events.size > 0 %}
<ul class="event-list">
  {% for event in events %}
  <li class="event-list-item">
    <div class="event-list-title"><a href="{{ event.url }}">{{ event.title }}</a></div>
    <div class="event-list-meta">{{ event.date | date: "%B %-d, %Y" }} &middot; {{ event.location }}</div>
  </li>
  {% endfor %}
</ul>
{% else %}
*No events yet.*
{% endif %}