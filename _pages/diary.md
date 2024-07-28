---
title: Diary
permalink: /diary/
---
<ul id="markdown-toc">
  <li><a href="#2024">2024</a></li>
  <li><a href="#2023">2023</a></li>
  <li><a href="#2022">2022</a></li>
  <li><a href="#2021">2021</a></li>
  <li><a href="#2020">2020</a></li>
  <li><a href="#2018">2018 (recovered)</a></li>
  <li><a href="#2017">2017</a></li>
  <li><a href="#2013">2013 (recovered)</a></li>
  <li><a href="#2004">2004 (recovered)</a></li>
  <li><a href="#2003">2003 (recovered)</a></li>
  <li><a href="#2002">2002 (recovered)</a></li>
  <li><a href="#poetry">poetry</a></li>
</ul>

{% for category in site.categories reversed %}
  <h2 id="{{ category | first | replace: '-', ' '  }}">{{ category | first | replace: '-', ' ' }} </h2>
  <ol reversed>
    {% for post in category.last  %}
      <li class="all-items"><span class="all-date">{{ post.date| date: "%b %d, %Y" }} - </span><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ol>
{% endfor %}

<h2 id="poetry">poetry</h2>

[...from 1997 to 2011](/diary/poetry/)

