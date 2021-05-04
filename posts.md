--- 
layout: page
title: All Posts
date: 2021-05-04 22:44
permalink: blog
author: Kevin Olega 
--- 

<p><iframe src="https://duckduckgo.com/search.html?site=minimalchanges.com&prefill=Search minimal changes" style="overflow:hidden;margin:0;padding:0;width:408px;height:40px;" frameborder="0"></iframe></p>
  

<h1 class="page-heading">ARTICLES</h1>
  
  {{ content }}

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>
