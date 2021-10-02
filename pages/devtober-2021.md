---
layout: page
title: Devtober 2021
permalink: /devtober-2021
weight: 0
regenerate: true
---

Devtober is a month all about staying productive day-to-day, even if that means just a little bit of work. Between participating in Ludum Dare 49 at the start of the month and a bunch of ideas I have floating around in my head, I'm looking forward to a fun month of awesome projects! Check out the blog posts below for a peak at what each day was like for me.  

{% for post in site.devtober-2021 reversed %}
  ---
  {% assign post_date = post.path | split: '/' | last | replace: '.md', '' %}
  <h3>{{ post.title }}</h3>
  <div style="display:flex;justify-content:flex-end"><h6> ({{ post_date }})</h6></div>
  <p>{{ post.content | markdownify}}</p>
{% endfor %}
