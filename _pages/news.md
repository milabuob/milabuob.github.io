---
layout: splash #category
title: "News"
classes: wide
permalink: /news/
taxonomy: news
---

<style>
  .news-container {
    display: flex;
    justify-content: space-between;
  }
  .news-content {
    width: 70%; /* Main content area for latest news */
  }
  .news-toc {
    width: 25%; /* Sidebar for table of contents */
    margin-left: 20px;
    position: sticky;
    top: 20px; /* Keeps the TOC visible while scrolling */
    background-color: #f9f9f9;
    padding: 15px;
    border-radius: 8px;
  }
  .news-toc ul {
    list-style-type: none;
    padding: 0;
  }
  .news-toc li {
    margin-bottom: 10px;
  }
</style>

## MILab News

<div class="news-container">

  <!-- Main News Content (Latest News) -->
  <div class="news-content">
    
    {% assign latest_news = site.posts | where: "categories", "news" | sort: "date" | reverse %}
    <ul>
      {% for post in latest_news limit: 10 %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a> <br>
          <small>{{ post.date | date: "%B %-d, %Y" }}</small>
        </li>
      {% endfor %}
    </ul>
  </div>

  <!-- Sidebar Table of Contents -->
  <div class="news-toc">
    <h3>Table of Contents</h3>
    <ul>
      {% assign sorted_posts = site.posts | where: "categories", "news" | sort: "date" | reverse %}
      {% assign posts_by_year = sorted_posts | group_by_exp: "post", "post.date | date: '%Y'" %}
      {% for year in posts_by_year %}
        <li><a href="#{{ year.name }}">{{ year.name }}</a></li>
      {% endfor %}
    </ul>
  </div>

</div>

---
