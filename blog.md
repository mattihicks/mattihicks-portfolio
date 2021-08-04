---
layout: default
image: aboutPicOG.jpg
---


<div class="home">

  <h1 class="post-heading"></h1>


  <ul class="post-list">
    {% for post in paginator.posts %}
      <li>
          <h2><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
        <div class="post-meta-front-page">{{ post.date | date: "%b %-d, %Y" }}</div> 
        <div class="post-meta-front"></div>

        {{ post.content }}



      </li>
    {% endfor %}
  </ul>




<div class="paginatorSupreme">






  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous-pagination">
      Previous
    </a>
  {% else %}
    <span class="previous"></span>
  {% endif %}


<span class="pageNum">
  Page {{ paginator.page }} of {{ paginator.total_pages }}
</span>


    {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next-pagination"> Next</a>
  {% else %}
    <div class="next-pagination "></div>
  {% endif %}
</div>













<!--   <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p> -->
</div>

<!-- <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a> -->
