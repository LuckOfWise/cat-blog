---
layout: default
---

# 最新の記事

{% for post in site.posts limit:10 %}
  <div style="margin-bottom: 30px; padding-bottom: 20px; border-bottom: 1px solid #eee;">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p class="post-date">{{ post.date | date: "%Y年%m月%d日" }}</p>
    <div>{{ post.excerpt }}</div>
  </div>
{% endfor %}
