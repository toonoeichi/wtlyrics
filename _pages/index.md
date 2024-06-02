---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to What the Lyrics!
## With all the weird , dirty , and everything that possible in the Lyrics!

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Remember! All the lyrics that appeared here aren't approved by Music Author, use it carefully. But it safe for personal use and you can sing (I mean yell it) at you friend's house or school!
</p>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
