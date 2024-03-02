---
layout: default
---

<!--
[Link to another page](./another-page.html).
-->

<!--
### Coming soon...

Hello! This is my personal webpage. Here I'll share research resources, datasets, code, papers and related stuff. For now, you can find many of these things in the above links.

<embed src="https://scrollprize.org/grandprize#runners-up" style="width:600px; height: 600px;">
-->

# News, posts, etc

<div class="blog-posts">
{% for post in site.posts %}
  <div class="post-preview">    
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="date">{{ post.date | date: "%b %-d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    {% if post.image %}
      <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="post-thumbnail">
    {% endif %}
    <br>
    <a href="{{ post.url | relative_url }}" class="read-more">Read More</a>
  </div>
{% endfor %}
</div>