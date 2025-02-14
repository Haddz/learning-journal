---
layout: default
title: "My Learning Journal"
---

{% assign homepage_posts = site.journal | where: "category", "homepage" %}

<h1>Welcome to My Learning Journal! 📖</h1>
<p>This is my personal space where I document everything I learn in Data Science, Tech, and Life.</p>

<h2>🔗 Quick Links</h2>
<ul>
  <li><a href="/learning-logs">📚 Learning Logs</a></li>
  <li><a href="/analytics-projects">📊 Analytics Projects</a></li>
  <li><a href="/resources">🌐 Resources</a></li>
</ul>

{% for post in homepage_posts %}
  <h2>{{ post.title }}</h2>
  <p>{{ post.content | truncatewords: 30 }}</p>
  <a href="{{ post.url }}">Read More</a>
{% endfor %}

[View Repository on GitHub](https://github.com/Haddz/learning-journal)
